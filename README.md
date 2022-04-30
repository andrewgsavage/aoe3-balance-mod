cd 'C:\Users\A\repos\\aoe3-balance-mod-official'
mkdir .temp

# Use Resource manager to extract data
File -> Open
    C:\Program Files (x86)\Steam\steamapps\common\AoE3DE\Game\Data\Data.bar
Extract -> All files
    Check xml and png options
    C:\Users\A\repos\aoe3-balance-mod-official\.temp

rm -r Data
mkdir Data
cp .temp/Data/techtreey.xml ./Data
cp .temp/Data/protoy.xml ./Data



rm -r .temp

mkdir .temp


C:\Program Files (x86)\Steam\steamapps\common\AoE3DE\Game\UI

rm -r UI
mv .temp/Data UI
rm -r .temp

    
# Commands to update data
    
git add -f aoe3_damage_calc/xml/homecity*.xml
git add -f aoe3_damage_calc/xml/protoy.xml
git add -f aoe3_damage_calc/xml/techtreey.xml
git add -f aoe3_damage_calc/UI/Data/wpfg/resources/images/icons/techs/
git add -f aoe3_damage_calc/UI/Data/wpfg/resources/images/icons/techs/native/
git add -f aoe3_damage_calc/UI/Data/wpfg/resources/images/icons/ingame/
git add -f aoe3_damage_calc/UI/Data/wpfg/resources/images/icons/home_city/