---
UID: NF:wingdi.EnumICMProfilesW
title: EnumICMProfilesW function (wingdi.h)
description: The EnumICMProfiles function enumerates the different output color profiles that the system supports for a given device context. (Unicode)
helpviewer_keywords: ["EnumICMProfiles", "EnumICMProfiles function [Windows Color System]", "EnumICMProfilesW", "_color_EnumICMProfiles", "wcs.enumicmprofiles", "wingdi/EnumICMProfiles", "wingdi/EnumICMProfilesW"]
old-location: wcs\enumicmprofiles.htm
tech.root: WCS
ms.assetid: a93e6239-b6c7-4e37-9f06-03790a3ed53f
ms.date: 12/05/2018
ms.keywords: EnumICMProfiles, EnumICMProfiles function [Windows Color System], EnumICMProfilesA, EnumICMProfilesW, _color_EnumICMProfiles, wcs.enumicmprofiles, wingdi/EnumICMProfiles, wingdi/EnumICMProfilesA, wingdi/EnumICMProfilesW
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - EnumICMProfilesW
 - wingdi/EnumICMProfilesW
dev_langs:
 - c++
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
---

# EnumICMProfilesW function


## -description

The <b>EnumICMProfiles</b> function enumerates the different output color profiles that the system supports for a given device context.

## -parameters

### -param hdc

Specifies the device context.

### -param proc

Specifies the procedure instance address of a callback function defined by the application. (See <a href="/windows/desktop/api/wingdi/nc-wingdi-icmenumproca">EnumICMProfilesProcCallback</a>.)

### -param param

Data supplied by the application that is passed to the callback function along with the color profile information.

## -returns

This function returns zero if the application interrupted the enumeration. The return value is -1 if there are no color profiles to enumerate. Otherwise, the return value is the last value returned by the callback function.

## -remarks

The <b>EnumICMProfiles</b> function returns a list of profiles that are associated with a device context (DC), and whose settings match those of the DC. It is possible for a device context to contain device profiles that are not associated with particular hardware devices, or device profiles that do not match the settings of the DC. The sRGB profile is an example. The <a href="/windows/desktop/api/wingdi/nf-wingdi-seticmprofilea">SetICMProfile</a> function is used to associate these types of profiles with a DC. The <a href="/windows/desktop/api/wingdi/nf-wingdi-geticmprofilea">GetICMProfile</a> function can be used to retrieve a profile that is not enumerated by the <b>EnumICMProfiles</b> function.

<b>Windows 95/98/Me:</b><b>EnumICMProfilesW</b> is supported by the Microsoft Layer for Unicode. To use this, you must add certain files to your application, as outlined in <a href="https://msdn.microsoft.com/library?url=/library/mslu/winprog/microsoft_layer_for_unicode_on_windows_95_98_me_systems.asp">Microsoft Layer for Unicode on Windows 95/98/Me Systems</a>.





> [!NOTE]
> The wingdi.h header defines EnumICMProfiles as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

* [Basic color management concepts](/windows/win32/wcs/basic-color-management-concepts)
* [Functions](/windows/win32/wcs/functions)
* [DeleteColorSpaceW](/windows/win32/api/wingdi/nf-wingdi-deletecolorspace)
* [ICMENUMPROCA callback function](/windows/win32/api/wingdi/nc-wingdi-icmenumproca)
* [GetICMProfileW](/windows/win32/api/wingdi/nf-wingdi-geticmprofilew)
* [SetICMProfileW](/windows/win32/api/wingdi/nf-wingdi-seticmprofilew)
