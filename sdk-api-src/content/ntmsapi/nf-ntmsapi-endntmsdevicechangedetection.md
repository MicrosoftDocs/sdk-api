---
UID: NF:ntmsapi.EndNtmsDeviceChangeDetection
title: EndNtmsDeviceChangeDetection function
author: windows-sdk-content
description: The EndNtmsDeviceChangeDetection function ends device change detection for any target devices specified using the SetNtmsDeviceChangeDetection function and closes the change detection handle.
old-location: fs\endntmsdevicechangedetection.htm
old-project: Rsm
ms.assetid: cb8dc379-30a1-43b0-b5a7-c6bc59b3e9ac
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: EndNtmsDeviceChangeDetection, EndNtmsDeviceChangeDetection function [Files], _zaw_endntmsdevicechangedetection, base.endntmsdevicechangedetection, fs.endntmsdevicechangedetection, ntmsapi/EndNtmsDeviceChangeDetection
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: ntmsapi.h
req.include-header: 
req.redist: 
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
 - EndNtmsDeviceChangeDetection
product: Windows
targetos: Windows
req.lib: Ntmsapi.lib
req.dll: Ntmsapi.dll
req.irql: 
req.product: ADAM
---

# EndNtmsDeviceChangeDetection function


## -description


<p class="CCE_Message">[<a href="https://msdn.microsoft.com/af7186f8-7921-48e3-a4fd-23259a6e9018">Removable Storage Manager</a> is no longer available as of Windows 7 and  Windows Server 2008 R2.]

The 
<b>EndNtmsDeviceChangeDetection</b> function ends device change detection for any target devices specified using the 
<a href="https://msdn.microsoft.com/803bd7d6-f098-42f1-83da-fe9f71f960b0">SetNtmsDeviceChangeDetection</a> function and closes the change detection handle.


## -parameters




### -param hSession [in]

Handle to the session returned by the 
<a href="https://msdn.microsoft.com/5a323911-e99c-4f81-9580-0feac2f0a54e">OpenNtmsSession</a> function


### -param DetectHandle [in]

Device change detection handle returned by the 
<a href="https://msdn.microsoft.com/d325a10a-5bf9-4431-8a6a-a50c4cf46728">BeginNtmsDeviceChangeDetection</a> function.


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
The session handle or detection handle is not valid.

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



Closing the Removable Storage Manager session also ends all device change detection sessions.




## -see-also




<a href="https://msdn.microsoft.com/d325a10a-5bf9-4431-8a6a-a50c4cf46728">BeginNtmsDeviceChangeDetection</a>



<a href="removable_storage_manager_functions.htm">Change Detection Functions</a>



<a href="https://msdn.microsoft.com/803bd7d6-f098-42f1-83da-fe9f71f960b0">SetNtmsDeviceChangeDetection</a>
 

 

