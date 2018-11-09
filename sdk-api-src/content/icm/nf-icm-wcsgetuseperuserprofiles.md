---
UID: NF:icm.WcsGetUsePerUserProfiles
title: WcsGetUsePerUserProfiles function
author: windows-sdk-content
description: Determines whether the user chose to use a per-user profile association list for the specified device.
old-location: wcs\wcsgetuseperuserprofiles.htm
tech.root: WCS
ms.assetid: 375a9ee6-b432-424a-8671-c5a598d82342
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: WcsGetUsePerUserProfiles, WcsGetUsePerUserProfiles function [Windows Color System], _color_WcsGetUsePerUserProfiles, icm/WcsGetUsePerUserProfiles, wcs.wcsgetuseperuserprofiles
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
 - WcsGetUsePerUserProfiles
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WcsGetUsePerUserProfiles function


## -description


Determines whether the user chose to use a per-user profile association list for the specified device.


## -parameters




### -param pDeviceName [in]

A pointer to a string containing the user-friendly name of the device.


### -param dwDeviceClass [in]

A flag value specifying the class of the device. This parameter must take one of the following values:

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
<td>Specifies an image-capture device.</td>
</tr>
</table>
 


### -param pUsePerUserProfiles [out]

A pointer to a location to receive a Boolean value that is <b>TRUE</b> if the user chose to use a per-user profile association list for the specified device; otherwise <b>FALSE</b>.


## -returns



If this function succeeds, the return value is <b>TRUE</b>.

If this function fails, the return value is <b>FALSE</b>. For extended error information, call <b>GetLastError</b>.




## -remarks



This function fails if <i>pDeviceName</i> points to a device that is not of the class specified by <i>dwDeviceClass</i>.

This function is executable in Least-Privileged User Account (LUA) context.




## -see-also




<a href="https://msdn.microsoft.com/a0623917-0b63-4546-a71a-1e9efa9fe8e5">Basic Color Management Concepts</a>



<a href="https://msdn.microsoft.com/ee9e9502-5514-4070-95fa-265674a1dde7">Functions</a>



<a href="https://msdn.microsoft.com/c108fbb2-e9f3-41fe-af36-99114df1507e">WcsSetUsePerUserProfiles</a>



<a href="https://msdn.microsoft.com/fa05ba0c-b01d-4d50-8769-94a6e19f0066">Windows Color System Schemas and Algorithms</a>
 

 

