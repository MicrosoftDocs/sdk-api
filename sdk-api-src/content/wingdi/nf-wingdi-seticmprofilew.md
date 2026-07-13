---
UID: NF:wingdi.SetICMProfileW
title: SetICMProfileW function (wingdi.h)
description: The SetICMProfile function sets a specified color profile as the output profile for a specified device context (DC). (Unicode)
helpviewer_keywords: ["SetICMProfile", "SetICMProfile function [Windows Color System]", "SetICMProfileW", "_color_SetICMProfile", "wcs.seticmprofile", "wingdi/SetICMProfile", "wingdi/SetICMProfileW"]
old-location: wcs\seticmprofile.htm
tech.root: WCS
ms.assetid: c95f6536-9377-4766-9eb6-004a41bcf6c5
ms.date: 12/05/2018
ms.keywords: SetICMProfile, SetICMProfile function [Windows Color System], SetICMProfileA, SetICMProfileW, _color_SetICMProfile, wcs.seticmprofile, wingdi/SetICMProfile, wingdi/SetICMProfileA, wingdi/SetICMProfileW
req.header: wingdi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SetICMProfileW (Unicode) and SetICMProfileA (ANSI)
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
 - SetICMProfileW
 - wingdi/SetICMProfileW
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
 - SetICMProfile
 - SetICMProfileA
 - SetICMProfileW
---

# SetICMProfileW function


## -description

The <b>SetICMProfile</b> function sets a specified color profile as the output profile for a specified device context (DC).

## -parameters

### -param hdc

Specifies a device context in which to set the color profile.

### -param lpFileName

Specifies the path name of the color profile to be set.

## -returns

If this function succeeds, the return value is <b>TRUE</b>.

If this function fails, the return value is <b>FALSE</b>.

## -remarks

<b>SetICMProfile</b> associates a color profile with a device context. It becomes the output profile for that device context. The color profile does not have to be associated with any particular device. Device-independent profiles such as sRGB can also be used. If the color profile is not associated with a hardware device, it will be returned by <a href="/windows/desktop/api/wingdi/nf-wingdi-geticmprofilea">GetICMProfile</a>, but not by <a href="/windows/desktop/api/wingdi/nf-wingdi-enumicmprofilesa">EnumICMProfiles</a>.

Note that under Windows 95 or later, the PostScript device driver for printers assumes a CMYK color model. Therefore, all PostScript printers must use a CMYK color profile. Windows 2000 does not have this limitation.

<b>SetICMProfile</b> supports only RGB profiles in compatible DCs.

<b>Windows 95/98/Me: </b><b>SetICMProfileW</b> is supported by the Microsoft Layer for Unicode. To use this, you must add certain files to your application, as outlined in <a href="https://msdn.microsoft.com/library?url=/library/mslu/winprog/microsoft_layer_for_unicode_on_windows_95_98_me_systems.asp">Microsoft Layer for Unicode on Windows 95/98/Me Systems</a>.





> [!NOTE]
> The wingdi.h header defines SetICMProfile as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

* [Basic color management concepts](/windows/win32/wcs/basic-color-management-concepts)
* [Functions](/windows/win32/wcs/functions)
* [EnumICMProfilesW](/windows/win32/api/wingdi/nf-wingdi-enumicmprofilesw)
* [GetICMProfileW](/windows/win32/api/wingdi/nf-wingdi-geticmprofilew)
