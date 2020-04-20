---
UID: NF:wingdi.EnumICMProfilesW
title: EnumICMProfilesW function (wingdi.h)
description: The EnumICMProfiles function enumerates the different output color profiles that the system supports for a given device context.helpviewer_keywords: ["EnumICMProfiles","EnumICMProfiles function [Windows Color System]","EnumICMProfilesA","EnumICMProfilesW","_color_EnumICMProfiles","wcs.enumicmprofiles","wingdi/EnumICMProfiles","wingdi/EnumICMProfilesA","wingdi/EnumICMProfilesW"]
old-location: wcs\enumicmprofiles.htm
tech.root: WCS
ms.assetid: a93e6239-b6c7-4e37-9f06-03790a3ed53f
ms.date: 12/05/2018
ms.keywords: EnumICMProfiles, EnumICMProfiles function [Windows Color System], EnumICMProfilesA, EnumICMProfilesW, _color_EnumICMProfiles, wcs.enumicmprofiles, wingdi/EnumICMProfiles, wingdi/EnumICMProfilesA, wingdi/EnumICMProfilesW
f1_keywords:
- wingdi/EnumICMProfiles
dev_langs:
- c++
req.header: wingdi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: EnumICMProfilesW (Unicode) and EnumICMProfilesA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Gdi32.dll
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32Full.dll
api_name:
- EnumICMProfiles
- EnumICMProfilesA
- EnumICMProfilesW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# EnumICMProfilesW function


## -description


The <b>EnumICMProfiles</b> function enumerates the different output color profiles that the system supports for a given device context.


## -parameters




### -param hdc

Specifies the device context.


### -param proc

Specifies the procedure instance address of a callback function defined by the application. (See <a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nc-wingdi-icmenumproca">EnumICMProfilesProcCallback</a>.)


### -param param

Data supplied by the application that is passed to the callback function along with the color profile information.


## -returns



This function returns zero if the application interrupted the enumeration. The return value is -1 if there are no color profiles to enumerate. Otherwise, the return value is the last value returned by the callback function.




## -remarks



The <b>EnumICMProfiles</b> function returns a list of profiles that are associated with a device context (DC), and whose settings match those of the DC. It is possible for a device context to contain device profiles that are not associated with particular hardware devices, or device profiles that do not match the settings of the DC. The sRGB profile is an example. The <a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-seticmprofilea">SetICMProfile</a> function is used to associate these types of profiles with a DC. The <a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-geticmprofilea">GetICMProfile</a> function can be used to retrieve a profile that is not enumerated by the <b>EnumICMProfiles</b> function.

<b>Windows 95/98/Me:</b><b>EnumICMProfilesW</b> is supported by the Microsoft Layer for Unicode. To use this, you must add certain files to your application, as outlined in <a href="https://msdn.microsoft.com/library?url=/library/mslu/winprog/microsoft_layer_for_unicode_on_windows_95_98_me_systems.asp">Microsoft Layer for Unicode on Windows 95/98/Me Systems</a>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/wcs/basic-color-management-concepts">Basic Color Management Concepts</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nc-wingdi-icmenumproca">EnumICMProfilesProcCallback</a>



<a href="https://docs.microsoft.com/previous-versions/dd316902(v=vs.85)">Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-geticmprofilea">GetICMProfile</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-seticmprofilea">SetICMProfile</a>
 

 

