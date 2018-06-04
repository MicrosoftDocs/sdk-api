---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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


### -param DetectHandle

TBD




#### - hDetectHandle [in]

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
 

 

