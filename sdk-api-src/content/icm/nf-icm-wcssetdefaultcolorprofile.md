---
UID: NF:icm.WcsSetDefaultColorProfile
title: WcsSetDefaultColorProfile function
author: windows-sdk-content
description: Sets the default color profile name for the specified profile type in the specified profile management scope.
old-location: wcs\wcssetdefaultcolorprofile.htm
tech.root: WCS
ms.assetid: 6f9e8df8-e696-4fd0-8631-5e3d23719def
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: WcsSetDefaultColorProfile, WcsSetDefaultColorProfile function [Windows Color System], _color_WcsSetDefaultColorProfile, icm/WcsSetDefaultColorProfile, wcs.wcssetdefaultcolorprofile
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: icm.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
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
 - WcsSetDefaultColorProfile
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- WcsSetDefaultColorProfile
: 
---

# WcsSetDefaultColorProfile function


## -description


Sets the default color profile name for the specified profile type in the specified profile management scope.


## -parameters




### -param scope

TBD


### -param pDeviceName [in, optional]

A pointer to the name of the device for which the default color profile is to be set. If <b>NULL</b>, a device-independent default profile is used.


### -param cptColorProfileType [in]

A <a href="https://msdn.microsoft.com/aaf6fd19-0693-4a76-812f-ff958eb5c944">COLORPROFILETYPE</a> value that specifies the color profile type.


### -param cpstColorProfileSubType [in]

A <a href="https://msdn.microsoft.com/b5cc965e-47b2-4309-8558-5208c7a2b587">COLORPROFILESUBTYPE</a> value that specifies the color profile subtype.


### -param dwProfileID [in]

The ID of the color space that the color profile represents. This is a custom ID value used to uniquely identify the color space profile within your application.


### -param pProfileName [in]

A pointer to a buffer that holds the name of the color profile. See Remarks.


#### - profileManagementScope [in]

A <a href="https://msdn.microsoft.com/6895a807-81da-4263-b370-977ecfaffac8">WCS_PROFILE_MANAGEMENT_SCOPE</a> value that specifies the scope of this profile management operation.


## -returns



If this function succeeds, the return value is <b>TRUE</b>.

If this function fails, the return value is <b>FALSE</b>. For extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



If the <i>pProfileName</i> parameter is <b>NULL</b> and the <i>profileManagementScope</i> parameter is WCS_PROFILE_MANAGEMENT_SCOPE_CURRENT_USER, subsequent calls to <b>WcsSetDefaultColorProfile</b> will return the system-wide default profile.

If <i>profileManagementScope</i> is WCS_PROFILE_MANAGEMENT_SCOPE_CURRENT_USER, this function is executable in Least-Privileged User Account (LUA) context. Otherwise, administrative privileges are required. The specified profile must already be installed, but it may be not yet associated with the specified device in the specified profile management scope.

When WcsSetDefaultColorProfile is called to set a device model profile DMP as the default profile for the RGB or custom working space, only a DMP profile that is of type RGBVirtualDevice, LCD, or CRT is valid; all others are invalid.

When WcsSetDefaultColorProfile is called to set an International Color Consortium (ICC) profile as the default profile for the RGB or custom working space, only an ICC profile with class "spac" or "disp", and "RGB" color space is valid; all others are invalid.

See notes on valid profile type/subtype combinations.




## -see-also




<a href="https://msdn.microsoft.com/a0623917-0b63-4546-a71a-1e9efa9fe8e5">Basic Color Management Concepts</a>



<a href="https://msdn.microsoft.com/b5cc965e-47b2-4309-8558-5208c7a2b587">COLORPROFILESUBTYPE</a>



<a href="https://msdn.microsoft.com/aaf6fd19-0693-4a76-812f-ff958eb5c944">COLORPROFILETYPE</a>



<a href="https://msdn.microsoft.com/ee9e9502-5514-4070-95fa-265674a1dde7">Functions</a>



<a href="https://msdn.microsoft.com/6895a807-81da-4263-b370-977ecfaffac8">WCS_PROFILE_MANAGEMENT_SCOPE</a>



<a href="https://msdn.microsoft.com/68f589ac-15e0-4d13-a2fa-e3f74d7d3d19">WcsGetDefaultColorProfileSize</a>



<a href="https://msdn.microsoft.com/fa05ba0c-b01d-4d50-8769-94a6e19f0066">Windows Color System Schemas and Algorithms</a>
 

 

