# Test page

```js [SculkSpine.java]
@Override
    public boolean canStart()
    {
        ticksElapsed++;

        if(getSculkEnderman().isSpecialAttackOnCooldown() || mob.getTarget() == null)
        {
            return false;
        }

        if(!mob.isInRange(mob.getTarget(), 12.0D) || !mob.getTarget().isOnGround())
        {
            return false;
        }

        if(ticksElapsed < executionCooldown)
        {
            return false;
        }

        return true;
    }
```

/
