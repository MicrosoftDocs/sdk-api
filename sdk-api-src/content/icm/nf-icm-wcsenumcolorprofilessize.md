---
UID: NF:icm.WcsEnumColorProfilesSize
title: WcsEnumColorProfilesSize function
author: windows-sdk-content
description: Returns the size, in bytes, of the buffer that is required by the WcsEnumColorProfiles function to enumerate color profiles.
old-location: wcs\wcsenumcolorprofilessize.htm
tech.root: WCS
ms.assetid: 1fc76f8a-dad5-4447-bffc-2df58b4201de
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: WcsEnumColorProfilesSize, WcsEnumColorProfilesSize function [Windows Color System], _color_WcsEnumColorProfilesSize, icm/WcsEnumColorProfilesSize, wcs.wcsenumcolorprofilessize
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
 - WcsEnumColorProfilesSize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WcsEnumColorProfilesSize function


## -description


Returns the size, in bytes, of the buffer that is required by the <a href="https://msdn.microsoft.com/45d670ae-a2f1-4281-bcd8-0663ee3e7fe4">WcsEnumColorProfiles</a> function to enumerate color profiles.


## -parameters




### -param scope

TBD


### -param pEnumRecord [in]

A pointer to a structure that specifies the enumeration criteria.


### -param pdwSize [out]

A pointer to a variable that receives the size of the buffer that is required to receive all enumerated profile names. This value is used by the <i>dwSize</i> parameter of the <a href="https://msdn.microsoft.com/45d670ae-a2f1-4281-bcd8-0663ee3e7fe4">WcsEnumColorProfiles</a> function.


#### - profileManagementScope [in]

A <a href="https://msdn.microsoft.com/6895a807-81da-4263-b370-977ecfaffac8">WCS_PROFILE_MANAGEMENT_SCOPE</a> value that specifies the scope of the profile management operation that is performed by this function.


## -returns



If this function succeeds, the return value is <b>TRUE</b>.

If this function fails, the return value is <b>FALSE</b>. For extended error information, call <b>GetLastError</b>.




## -remarks



This function is executable in Least-Privileged User Account (LUA) context.




## -see-also




<a href="https://msdn.microsoft.com/a0623917-0b63-4546-a71a-1e9efa9fe8e5">Basic Color Management Concepts</a>



<a href="https://msdn.microsoft.com/ee9e9502-5514-4070-95fa-265674a1dde7">Functions</a>



<a href="https://msdn.microsoft.com/6895a807-81da-4263-b370-977ecfaffac8">WCS_PROFILE_MANAGEMENT_SCOPE</a>



<a href="https://msdn.microsoft.com/45d670ae-a2f1-4281-bcd8-0663ee3e7fe4">WcsEnumColorProfiles</a>



<a href="https://msdn.microsoft.com/fa05ba0c-b01d-4d50-8769-94a6e19f0066">Windows Color System Schemas and Algorithms</a>
 

 

