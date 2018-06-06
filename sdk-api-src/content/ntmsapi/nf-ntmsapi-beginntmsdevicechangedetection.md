---
UID: NF:ntmsapi.BeginNtmsDeviceChangeDetection
title: BeginNtmsDeviceChangeDetection function
author: windows-sdk-content
description: The BeginNtmsDeviceChangeDetection function allows the application to begin a device change detection session.
old-location: fs\beginntmsdevicechangedetection.htm
old-project: Rsm
ms.assetid: d325a10a-5bf9-4431-8a6a-a50c4cf46728
ms.author: windowssdkdev
ms.date: 04/05/2018
ms.keywords: BeginNtmsDeviceChangeDetection, BeginNtmsDeviceChangeDetection function [Files], _zaw_beginntmsdevicechangedetection, base.beginntmsdevicechangedetection, fs.beginntmsdevicechangedetection, ntmsapi/BeginNtmsDeviceChangeDetection
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: ntmsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ntmsapi.dll
api_name:
 - BeginNtmsDeviceChangeDetection
product: Windows
targetos: Windows
req.lib: Ntmsapi.lib
req.dll: Ntmsapi.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# BeginNtmsDeviceChangeDetection function


## -description


<p class="CCE_Message">[<a href="https://msdn.microsoft.com/af7186f8-7921-48e3-a4fd-23259a6e9018">Removable Storage Manager</a> is no longer available as of Windows 7 and  Windows Server 2008 R2.]

The 
<b>BeginNtmsDeviceChangeDetection</b> function allows the application to begin a device change detection session.


## -parameters




### -param hSession [in]

Handle to the session returned by the 
<a href="https://msdn.microsoft.com/5a323911-e99c-4f81-9580-0feac2f0a54e">OpenNtmsSession</a> function.


### -param lpDetectHandle [out]

Pointer to variable that receives the device change detection handle.


## -returns



This function returns one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The value of the <i>hSession</i> parameter is not a valid session handle.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The operator request has been canceled.

</td>
</tr>
</table>
 




## -remarks



After calling 
<b>BeginNtmsDeviceChangeDetection</b>, the application can set the stand-alone libraries for which media change detection is required using the 
<a href="https://msdn.microsoft.com/803bd7d6-f098-42f1-83da-fe9f71f960b0">SetNtmsDeviceChangeDetection</a> function. The Removable Storage Manager continues to detect changes for the devices specified until the change detection session is closed using the 
<a href="https://msdn.microsoft.com/cb8dc379-30a1-43b0-b5a7-c6bc59b3e9ac">EndNtmsDeviceChangeDetection</a> function.




## -see-also




<a href="removable_storage_manager_functions.htm">Change Detection Functions</a>



<a href="https://msdn.microsoft.com/cb8dc379-30a1-43b0-b5a7-c6bc59b3e9ac">EndNtmsDeviceChangeDetection</a>



<a href="https://msdn.microsoft.com/803bd7d6-f098-42f1-83da-fe9f71f960b0">SetNtmsDeviceChangeDetection</a>
 

 

