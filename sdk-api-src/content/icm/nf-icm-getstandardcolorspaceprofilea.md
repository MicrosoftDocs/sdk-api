---
UID: NF:icm.GetStandardColorSpaceProfileA
title: GetStandardColorSpaceProfileA function
author: windows-sdk-content
description: The GetStandardColorSpaceProfile function retrieves the color profile registered for the specified standard color space.
old-location: wcs\getstandardcolorspaceprofile.htm
tech.root: WCS
ms.assetid: b00f5c5c-f536-4d88-b61f-d2bdd0b180a0
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: GetStandardColorSpaceProfile, GetStandardColorSpaceProfile function [Windows Color System], GetStandardColorSpaceProfileA, GetStandardColorSpaceProfileW, _color_GetStandardColorSpaceProfile, icm/GetStandardColorSpaceProfile, icm/GetStandardColorSpaceProfileA, icm/GetStandardColorSpaceProfileW, wcs.getstandardcolorspaceprofile
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
req.unicode-ansi: GetStandardColorSpaceProfileW (Unicode) and GetStandardColorSpaceProfileA (ANSI)
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
 - Mscms.dll
api_name:
 - GetStandardColorSpaceProfile
 - GetStandardColorSpaceProfileA
 - GetStandardColorSpaceProfileW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetStandardColorSpaceProfileA function


## -description


The <b>GetStandardColorSpaceProfile</b> function retrieves the color profile registered for the specified standard <a href="c.htm">color space</a>.


## -parameters




### -param pMachineName

Reserved. Must be <b>NULL</b>. This parameter is intended to point to the name of the computer on which to get a standard color space profile. A <b>NULL</b> pointer indicates the local machine.


### -param dwSCS

TBD


### -param pBuffer

TBD


### -param pcbSize

TBD




#### - dwProfileID

Specifies the ID value of the standard color space for which to retrieve the profile. The only valid values for this parameter are LCS_sRGB and LCS_WINDOWS_COLOR_SPACE.


#### - pProfileName

Pointer to the buffer in which the name of the profile is to be placed. If <b>NULL</b>, the call will return <b>TRUE</b> and the required size of the buffer is placed in <i>pdwSize.</i>


#### - pdwSize

Pointer to a variable containing the size in bytes of the buffer pointed to by <i>pProfileName</i>. On return, the variable contains the size of the buffer actually used or needed.


## -returns



If this function succeeds, the return value is <b>TRUE</b>.

If this function fails, the return value is <b>FALSE</b>. For extended error information, call <b>GetLastError</b>.




## -remarks



If the buffer pointed to by <i>pProfileName</i> is to be dynamically allocated by an application, the application can call the <b>GetStandardColorSpaceProfile</b> function to retrieve the size required for the buffer. If <b>GetStandardColorSpaceProfile</b> is called with <i>pProfileName</i> set to <b>NULL</b>, it will return <b>FALSE</b> and the <b>DWORD</b> pointed at by <i>pdwSize</i> will contain the number of bytes needed for the buffer pointed at by <i>pProfileName</i>. The application can then allocate the buffer and call <b>GetStandardColorSpaceProfile</b> again with <i>pProfileName</i> set to the address of the buffer.

This function supports Windows Color System (WCS) device model profiles (DMPs) in addition to International Color Consortium (ICC) profiles. It does not support WCS CAMP or GMMP profiles and will return an error if such profiles are used.

<b>Overview of Windows Vista Specific Functionality</b>

This will support WCS DMPs in addition to ICC profiles. It will not support WCS CAMP or GMMP profiles and will return an error if such profiles are used with this API.

<b><i>Per-user/LUA support</i></b>

This will retrieve the color profile registered for the given standard color space for current user. If there is no such setting for the current user, it retrieves the system wide setting.

This uses <b>WcsGetDefaultColorProfile</b> with WCS_PROFILE_MANAGEMENT_SCOPE_CURRENT_USER.

This is executable in LUA context.




## -see-also




<a href="https://msdn.microsoft.com/a0623917-0b63-4546-a71a-1e9efa9fe8e5">Basic Color Management Concepts</a>



<a href="https://msdn.microsoft.com/ee9e9502-5514-4070-95fa-265674a1dde7">Functions</a>



<a href="https://msdn.microsoft.com/fb1d95f0-7f6c-4ad9-a382-459833f177f5">SetStandardColorSpaceProfile</a>
 

 

