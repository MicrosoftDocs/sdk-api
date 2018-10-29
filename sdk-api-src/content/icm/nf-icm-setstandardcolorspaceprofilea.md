---
UID: NF:icm.SetStandardColorSpaceProfileA
title: SetStandardColorSpaceProfileA function
author: windows-sdk-content
description: The SetStandardColorSpaceProfile function registers a specified profile for a given standard color space. The profile can be queried using GetStandardColorSpaceProfile.
old-location: wcs\setstandardcolorspaceprofile.htm
tech.root: WCS
ms.assetid: fb1d95f0-7f6c-4ad9-a382-459833f177f5
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: SetStandardColorSpaceProfile, SetStandardColorSpaceProfile function [Windows Color System], SetStandardColorSpaceProfileA, SetStandardColorSpaceProfileW, _color_SetStandardColorSpaceProfile, icm/SetStandardColorSpaceProfile, icm/SetStandardColorSpaceProfileA, icm/SetStandardColorSpaceProfileW, wcs.setstandardcolorspaceprofile
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: icm.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SetStandardColorSpaceProfileW (Unicode) and SetStandardColorSpaceProfileA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mscms.lib
req.dll: Mscms.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mscms.dll
api_name:
 - SetStandardColorSpaceProfile
 - SetStandardColorSpaceProfileA
 - SetStandardColorSpaceProfileW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SetStandardColorSpaceProfileA function


## -description


The <b>SetStandardColorSpaceProfile</b> function registers a specified profile for a given standard <a href="c.htm">color space</a>. The profile can be queried using <a href="https://msdn.microsoft.com/b00f5c5c-f536-4d88-b61f-d2bdd0b180a0">GetStandardColorSpaceProfile</a>.


## -parameters




### -param pMachineName

Reserved. Must be <b>NULL</b>. This parameter is intended to point to the name of the machine on which to set a standard color space profile. A <b>NULL</b> pointer indicates the local machine.


### -param dwProfileID

Specifies the ID value of the standard color space that the given profile represents. This is a custom ID value used to uniquely identify the color space profile within your application.


### -param pProfilename

Points to a fully qualified path to the profile file.


## -returns



If this function succeeds, the return value is <b>TRUE</b>.

If this function fails, the return value is <b>FALSE</b>. For extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The profile must already be installed on the system before it can be registered for a standard color space.

This function supports Windows Color System (WCS) device model profiles (DMPs) in addition to International Color Consortium (ICC) profiles. It does not support WCS CAMP or GMMP profiles and will return an error if such profiles are used.

<b><i>Per-user/LUA support</i></b>

This will register a specified profile for a given standard color space only for current user.

This uses <b>WcsSetDefaultColorProfile</b> with WCS_PROFILE_MANAGEMENT_SCOPE_CURRENT_USER.

This is executable in LUA context if the profile is already installed, fails otherwise with access denied since install is system-wide and requires administrator privileges.




## -see-also




<a href="https://msdn.microsoft.com/a0623917-0b63-4546-a71a-1e9efa9fe8e5">Basic Color Management Concepts</a>



<a href="https://msdn.microsoft.com/ee9e9502-5514-4070-95fa-265674a1dde7">Functions</a>



<a href="https://msdn.microsoft.com/b00f5c5c-f536-4d88-b61f-d2bdd0b180a0">GetStandardColorSpaceProfile</a>
 

 

