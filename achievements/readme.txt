This plugin allows you to add unlockable achievements to your ghost and for the user to see them!

Example usage:
1. sending achievements for the first time

_names = "Jarred|Pickled|Grass Land"
_desc = "U've been jarred|What a pickle|It's grassy in ere"
_hint = 1

"\![raiseplugin,Achievements,OnGetAchievements,Jar,%(_names),%(_desc),%(_hint)]"
//Ghost Name, names speparated with |, descriptions separated with |, show description before unlocking? 1 = yes|0 = no
      
2. Unlocking\Locking

if reference0 == "unlock";"\![raiseplugin,Achievements,OnLockUnlock,Jar,1,1]"
elseif reference0 == "lock";"\![raiseplugin,Achievements,OnLockUnlock,Jar,1,0]"
elseif reference0 == "unlock all";"\![raiseplugin,Achievements,OnLockUnlock,Jar,all,1]"
elseif reference0 == "lock all";"\![raiseplugin,Achievements,OnLockUnlock,Jar,all,0]"
//Ghost name, id of the achievement|all, 1 = unlock|0 = lock

3. Updating Achievements

_names = "Pickled Brain|Aquarium"
_desc = "Brain in a jar|iz fish"
    
if reference0 == "add"
{
    "\![raiseplugin,Achievements,OnAchievementUpdate,Jar,add,%(_names),%(_desc)]"
         //Ghost Name, add, achievement names to add separated with | if multiple,  achievement descriptions to add separated with | if multiple
}
elseif reference0 == "change"
{
    "\![raiseplugin,Achievements,OnAchievementUpdate,Jar,change,1,Pickled two: electric boogalo,What a pickle again]"
///Ghost name, change, id of the achievement,new name,new description
}
