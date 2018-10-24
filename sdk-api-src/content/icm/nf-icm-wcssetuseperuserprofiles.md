---
UID: NF:icm.WcsSetUsePerUserProfiles
title: WcsSetUsePerUserProfiles function
author: windows-sdk-content
description: Enables a user to specify whether or not to use a per-user profile association list for the specified device.
old-location: wcs\wcssetuseperuserprofiles.htm
tech.root: WCS
ms.assetid: c108fbb2-e9f3-41fe-af36-99114df1507e
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: WcsSetUsePerUserProfiles, WcsSetUsePerUserProfiles function [Windows Color System], _color_WcsSetUsePerUserProfiles, icm/WcsSetUsePerUserProfiles, wcs.wcssetuseperuserprofiles
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
 - WcsSetUsePerUserProfiles
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WcsSetUsePerUserProfiles function


## -description


Enables a user to specify whether or not to use a per-user profile association list for the specified device.


## -parameters




### -param pDeviceName [in]

A pointer to a string that contains the user-friendly name of the device.


### -param dwDeviceClass [in]

A flag value that specifies the class of the device. This parameter must take one of the following values:

<table>
<tr>
<td>CLASS_MONITOR</td>
<td>Specifies a display device.</td>
</tr>
<tr>
<td>CLASS_PRINTER</td>
<td>Specifies a printer.</td>
</tr>
<tr>
<td>CLASS_SCANNER</td>
<td>Specifies an image capture device.</td>
</tr>
</table>
 


### -param usePerUserProfiles [in]

A Boolean value that is TRUE if the user wants to use a per-user profile association list for the specified device; otherwise <b>FALSE</b>.


## -returns



If this function succeeds, the return value is <b>TRUE</b>.

If this function fails, the return value is <b>FALSE</b>. For extended error information, call <b>GetLastError</b>.




## -remarks



If <i>usePerUserProfiles</i> is <b>TRUE</b>, and the user is not already using a per-user profile association list for <i>pDeviceName</i>, then the per-user profile association list is initialized by making a copy of the system-wide profile association list for the same device. From then on, changes to the system-wide list are not included in the per-user list.

This function is executable in Least-Privileged User Account (LUA) context.




## -see-also




<a href="https://msdn.microsoft.com/a0623917-0b63-4546-a71a-1e9efa9fe8e5">Basic Color Management Concepts</a>



<a href="https://msdn.microsoft.com/ee9e9502-5514-4070-95fa-265674a1dde7">Functions</a>



<a href="https://msdn.microsoft.com/375a9ee6-b432-424a-8671-c5a598d82342">WcsGetUsePerUserProfiles</a>



<a href="https://msdn.microsoft.com/fa05ba0c-b01d-4d50-8769-94a6e19f0066">Windows Color System Schemas and Algorithms</a>
 

 

