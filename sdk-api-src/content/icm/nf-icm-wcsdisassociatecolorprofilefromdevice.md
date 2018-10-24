---
UID: NF:icm.WcsDisassociateColorProfileFromDevice
title: WcsDisassociateColorProfileFromDevice function
author: windows-sdk-content
description: Disassociates a specified WCS color profile from a specified device on a computer.
old-location: wcs\wcsdisassociatecolorprofilefromdevice.htm
tech.root: WCS
ms.assetid: d5c2ee77-7cab-4f41-801c-bc749bba00c1
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: WcsDisassociateColorProfileFromDevice, WcsDisassociateColorProfileFromDevice function [Windows Color System], _color_WcsDisassociateColorProfileFromDevice, icm/WcsDisassociateColorProfileFromDevice, wcs.wcsdisassociatecolorprofilefromdevice
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
 - WcsDisassociateColorProfileFromDevice
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WcsDisassociateColorProfileFromDevice function


## -description


Disassociates a specified WCS color profile from a specified device on a computer.


## -parameters




### -param scope

TBD


### -param pProfileName [in]

A pointer to the file name of the profile to disassociate.


### -param pDeviceName [in]

A pointer to the name of the device from which to disassociate the profile.


#### - profileManagementScope [in]

A <a href="https://msdn.microsoft.com/6895a807-81da-4263-b370-977ecfaffac8">WCS_PROFILE_MANAGEMENT_SCOPE</a> value that specifies the scope of this profile management operation, which could be system-wide or for the current user.


## -returns



If this function succeeds, the return value is <b>TRUE</b>.

If this function fails, the return value is <b>FALSE</b>. For extended error information, call <b>GetLastError</b>.




## -remarks



The WCS color profile should be installed. Moreover, you must use the same <i>profileManagementScope</i> value as when the device was associated with the profile. See <a href="https://msdn.microsoft.com/4a4c9175-6af4-4bc3-9a44-1f1614e7240d">WcsAssociateColorProfileWithDevice</a>.

If <i>profileManagementScope</i> is WCS_PROFILE_MANAGEMENT_SCOPE_SYSTEM_WIDE, the profile disassociation is systemwide and applies to all users. If <i>profileManagementScope</i> is WCS_PROFILE_MANAGEMENT_SCOPE_CURRENT_USER, the disassociation is only for the current user.

If more than one color profile is associated with a device, WCS uses the last associated profile as the default. For example, if your application sequentially associates three profiles with a device, WCS uses the last profile associated as the default. If your application then calls the <b>WcsDisassociateColorProfileFromDevice</b> function to disassociate the third profile (which is the default in this example), WCS uses the second profile as the default.

If your application disassociates all profiles from a device, WCS uses the sRGB profile as the default.

If <i>profileManagementScope</i> is WCS_PROFILE_MANAGEMENT_SCOPE_CURRENT_USER, this function is executable in Least-Privileged User Account (LUA) context. Otherwise, administrative privileges are required.




## -see-also




<a href="https://msdn.microsoft.com/a0623917-0b63-4546-a71a-1e9efa9fe8e5">Basic Color Management Concepts</a>



<a href="https://msdn.microsoft.com/ee9e9502-5514-4070-95fa-265674a1dde7">Functions</a>



<a href="https://msdn.microsoft.com/4a4c9175-6af4-4bc3-9a44-1f1614e7240d">WcsAssociateColorProfileWithDevice</a>



<a href="https://msdn.microsoft.com/fa05ba0c-b01d-4d50-8769-94a6e19f0066">Windows Color System Schemas and Algorithms</a>
 

 

