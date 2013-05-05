Detect Mobile
=============

Lightweight PHP plugin for EE2 that detects a mobile browser using the PHP Detect Mobile class (http://mobiledetect.net/)

Basic Usage
=============

**Check if any mobile device**

*Returns true or false for use in conditionals see later examples*

```{exp:detect_mobile:ismobile}```
        
**Check if not a mobile device**

```{exp:detect_mobile:isnotmobile}```
        
**Check if tablet**

```{exp:detect_mobile:istablet}```
        
**Check if phone***

```{exp:detect_mobile:isphone}```
        
###Conditional check for a mobile device

    {if '{exp:detect_mobile:ismobile}'}
        I am a mobile device
    {if:else}        
        I am not a mobile device
    {/if}
        
**Redirect any mobile device including tablets**

```{exp:detect_mobile:redirect location="mobile.mysite.com"}```
        
**Redirect all non-tablet mobile devices**

```{exp:detect_mobile:redirect location="mobile.mysite.com" tablet="no"}```
        
**Redirect just tablets and not mobiles**

```{exp:detect_mobile location="tablet.mysite.com" mobile="no"}```
        
**Seperate redirect locations for tablets and mobiles**

```{exp:detect_mobile tablet_location="tablet.mysite.com" location="mobile.mysite.com"}```
        
**Check for device type**

```{exp:detect_mobile:type}```

*returns phone, tablet or none*

###Conditional check for device type

    {if '{exp:detect_mobile:type}' == "tablet"}	
        I am a tablet
    {if:elseif '{exp:detect_mobile:type}' == "phone"}	
        I am a mobile phone
    {if:else}
        I am not a mobile device
    {/if}

**Check for platform**

```{{exp:detect_mobile:platform platform="Kindle"}}```

*Supported platform values: iPhone, BlackBerry, HTC, Nexus, Dell, Motorola, Samsung, LG, Sony, Asus, Palm, Vertu, Pantech, Fly, SimValley, GenericPhone, iPad, NexusTablet, SamsungTablet, Kindle, SurfaceTablet, AsusTablet, BlackBerryTablet, HTCtablet, MotorolaTablet, NookTablet, AcerTablet, ToshibaTablet, LGTablet, YarvikTablet, MedionTablet, ArnovaTablet, ArchosTablet, AinolTablet, SonyTablet, CubeTablet, CobyTablet, SMiTTablet, RockChipTablet, TelstraTablet, FlyTablet, bqTablet, HuaweiTablet, NecTablet, PantechTablet, BronchoTablet, VersusTablet, ZyncTablet, PositivoTablet, NabiTablet, PlaystationTablet, GenericTablet, AndroidOS, BlackBerryOS, PalmOS, SymbianOS, WindowsMobileOS, WindowsPhoneOS, iOS, MeeGoOS, MaemoOS, JavaOS, webOS, badaOS, BREWOS, Chrome, Dolfin, Opera, Skyfire, IE, Firefox, Bolt, TeaShark, Blazer, Safari, Tizen, UCBrowser, DiigoBrowser, Puffin, Mercury, GenericBrowser*
