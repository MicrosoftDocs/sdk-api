---
UID: NF:wingdi.SetICMProfileA
title: SetICMProfileA function
author: windows-driver-content
description: The SetICMProfile function sets a specified color profile as the output profile for a specified device context (DC).
old-location: wcs\seticmprofile.htm
old-project: WCS
ms.assetid: c95f6536-9377-4766-9eb6-004a41bcf6c5
ms.author: windowsdriverdev
ms.date: 5/17/2018
ms.keywords: SetICMProfile, SetICMProfile function [Windows Color System], SetICMProfileA, SetICMProfileW, _color_SetICMProfile, wcs.seticmprofile, wingdi/SetICMProfile, wingdi/SetICMProfileA, wingdi/SetICMProfileW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.typenames: DISPLAYCONFIG_VIDEO_OUTPUT_TECHNOLOGY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Gdi32.dll
-	Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
-	GDI32Full.dll
api_name:
-	SetICMProfile
-	SetICMProfileA
-	SetICMProfileW
product: Windows
targetos: Windows
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# SetICMProfileA function


## -description


The <b>SetICMProfile</b> function sets a specified color profile as the output profile for a specified device context (DC).


## -parameters




### -param hdc

TBD


### -param lpFileName

Specifies the path name of the color profile to be set.


#### - hDC

Specifies a device context in which to set the color profile.


## -returns



If this function succeeds, the return value is <b>TRUE</b>.

If this function fails, the return value is <b>FALSE</b>.




## -remarks



<b>SetICMProfile</b> associates a color profile with a device context. It becomes the output profile for that device context. The color profile does not have to be associated with any particular device. Device-independent profiles such as sRGB can also be used. If the color profile is not associated with a hardware device, it will be returned by <a href="https://msdn.microsoft.com/1e16771a-80c5-47bb-9c98-14169d4dd773">GetICMProfile</a>, but not by <a href="https://msdn.microsoft.com/a93e6239-b6c7-4e37-9f06-03790a3ed53f">EnumICMProfiles</a>.

Note that under Windows 95 or later, the PostScript device driver for printers assumes a CMYK color model. Therefore, all PostScript printers must use a CMYK color profile. Windows 2000 does not have this limitation.

<b>SetICMProfile</b> supports only RGB profiles in compatible DCs.

<b>Windows 95/98/Me: </b><b>SetICMProfileW</b> is supported by the Microsoft Layer for Unicode. To use this, you must add certain files to your application, as outlined in <a href="http://msdn.microsoft.com/library/default.asp?url=/library/en-us/mslu/winprog/microsoft_layer_for_unicode_on_windows_95_98_me_systems.asp">Microsoft Layer for Unicode on Windows 95/98/Me Systems</a>.




## -see-also




<a href="https://msdn.microsoft.com/a0623917-0b63-4546-a71a-1e9efa9fe8e5">Basic Color Management Concepts</a>



<a href="https://msdn.microsoft.com/a93e6239-b6c7-4e37-9f06-03790a3ed53f">EnumICMProfiles</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>



<a href="https://msdn.microsoft.com/1e16771a-80c5-47bb-9c98-14169d4dd773">GetICMProfile</a>
 

 

