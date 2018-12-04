---
UID: NF:wingdi.EnumICMProfilesW
title: EnumICMProfilesW function
author: windows-sdk-content
description: The EnumICMProfiles function enumerates the different output color profiles that the system supports for a given device context.
old-location: wcs\enumicmprofiles.htm
tech.root: WCS
ms.assetid: a93e6239-b6c7-4e37-9f06-03790a3ed53f
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: EnumICMProfiles, EnumICMProfiles function [Windows Color System], EnumICMProfilesA, EnumICMProfilesW, _color_EnumICMProfiles, wcs.enumicmprofiles, wingdi/EnumICMProfiles, wingdi/EnumICMProfilesA, wingdi/EnumICMProfilesW
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# EnumICMProfilesW function


## -description


The <b>EnumICMProfiles</b> function enumerates the different output color profiles that the system supports for a given device context.


## -parameters




### -param hdc

Specifies the device context.


### -param proc

Specifies the procedure instance address of a callback function defined by the application. (See <a href="https://msdn.microsoft.com/6e8f4ce5-c546-4e6a-8f35-4a22d60b6754">EnumICMProfilesProcCallback</a>.)


### -param param

Data supplied by the application that is passed to the callback function along with the color profile information.


## -returns



This function returns zero if the application interrupted the enumeration. The return value is -1 if there are no color profiles to enumerate. Otherwise, the return value is the last value returned by the callback function.




## -remarks



The <b>EnumICMProfiles</b> function returns a list of profiles that are associated with a device context (DC), and whose settings match those of the DC. It is possible for a device context to contain device profiles that are not associated with particular hardware devices, or device profiles that do not match the settings of the DC. The sRGB profile is an example. The <a href="https://msdn.microsoft.com/c95f6536-9377-4766-9eb6-004a41bcf6c5">SetICMProfile</a> function is used to associate these types of profiles with a DC. The <a href="https://msdn.microsoft.com/1e16771a-80c5-47bb-9c98-14169d4dd773">GetICMProfile</a> function can be used to retrieve a profile that is not enumerated by the <b>EnumICMProfiles</b> function.

<b>Windows 95/98/Me:</b><b>EnumICMProfilesW</b> is supported by the Microsoft Layer for Unicode. To use this, you must add certain files to your application, as outlined in <a href="http://msdn.microsoft.com/library/default.asp?url=/library/en-us/mslu/winprog/microsoft_layer_for_unicode_on_windows_95_98_me_systems.asp">Microsoft Layer for Unicode on Windows 95/98/Me Systems</a>.




## -see-also




<a href="https://msdn.microsoft.com/a0623917-0b63-4546-a71a-1e9efa9fe8e5">Basic Color Management Concepts</a>



<a href="https://msdn.microsoft.com/6e8f4ce5-c546-4e6a-8f35-4a22d60b6754">EnumICMProfilesProcCallback</a>



<a href="https://msdn.microsoft.com/ee9e9502-5514-4070-95fa-265674a1dde7">Functions</a>



<a href="https://msdn.microsoft.com/1e16771a-80c5-47bb-9c98-14169d4dd773">GetICMProfile</a>



<a href="https://msdn.microsoft.com/c95f6536-9377-4766-9eb6-004a41bcf6c5">SetICMProfile</a>
 

 

