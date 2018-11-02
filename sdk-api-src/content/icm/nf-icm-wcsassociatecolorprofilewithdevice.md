---
UID: NF:icm.WcsAssociateColorProfileWithDevice
title: WcsAssociateColorProfileWithDevice function
author: windows-sdk-content
description: Associates a specified WCS color profile with a specified device.
old-location: wcs\wcsassociatecolorprofilewithdevice.htm
tech.root: WCS
ms.assetid: 4a4c9175-6af4-4bc3-9a44-1f1614e7240d
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: WcsAssociateColorProfileWithDevice, WcsAssociateColorProfileWithDevice function [Windows Color System], WcsAssociateColorProfileWithDeviceA, WcsAssociateColorProfileWithDeviceW, _color_WcsAssociateColorProfileWithDevice, icm/WcsAssociateColorProfileWithDevice, icm/WcsAssociateColorProfileWithDeviceA, icm/WcsAssociateColorProfileWithDeviceW, wcs.wcsassociatecolorprofilewithdevice
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
req.unicode-ansi: WcsAssociateColorProfileWithDeviceW (Unicode) and WcsAssociateColorProfileWithDeviceA (ANSI)
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
 - WcsAssociateColorProfileWithDevice
 - WcsAssociateColorProfileWithDeviceA
 - WcsAssociateColorProfileWithDeviceW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WcsAssociateColorProfileWithDevice function


## -description


Associates a specified WCS color profile with a specified device.


## -parameters




### -param scope

TBD


### -param pProfileName [in]

A pointer to the file name of the profile to associate.


### -param pDeviceName [in]

A pointer to the name of the device with which the profile is to be associated.


#### - profileManagementScope [in]

A <a href="https://msdn.microsoft.com/6895a807-81da-4263-b370-977ecfaffac8">WCS_PROFILE_MANAGEMENT_SCOPE</a> value that specifies the scope of this profile management operation, which could be system-wide or for the current user.


## -returns



If this function succeeds, the return value is <b>TRUE</b>.

If this function fails, the return value is <b>FALSE</b>. For extended error information, call <b>GetLastError</b>.




## -remarks



The <b>WCSAssociateColorProfileWithDevice</b> function fails if the profile has not been installed on the computer using the <a href="https://msdn.microsoft.com/494b2080-a0a8-4fda-bc12-3bf196a6840c">InstallColorProfile</a> function.

If the <i>profileManagementScope</i> parameter is WCS_PROFILE_MANAGEMENT_SCOPE_SYSTEM_WIDE, the profile association is system-wide and applies to all users. If <i>profileManagementScope</i> is WCS_PROFILE_MANAGEMENT_SCOPE_CURRENT_USER, the association is only for the current user.

This function is executable in Least-Privileged User Account (LUA) context if <i>profileManagementScope</i> is WCS_PROFILE_MANAGEMENT_SCOPE_CURRENT_USER. Otherwise, administrative privileges are required.




## -see-also




<a href="https://msdn.microsoft.com/a0623917-0b63-4546-a71a-1e9efa9fe8e5">Basic Color Management Concepts</a>



<a href="https://msdn.microsoft.com/ee9e9502-5514-4070-95fa-265674a1dde7">Functions</a>



<a href="https://msdn.microsoft.com/d5c2ee77-7cab-4f41-801c-bc749bba00c1">WcsDisassociateColorProfileFromDevice</a>



<a href="https://msdn.microsoft.com/fa05ba0c-b01d-4d50-8769-94a6e19f0066">Windows Color System Schemas and Algorithms</a>
 

 

