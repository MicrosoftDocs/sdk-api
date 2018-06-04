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

# IEmptyVolumeCacheCallBack::PurgeProgress


## -description


Called periodically by a disk cleanup handler to update the disk cleanup manager on the progress of a purge of deletable files.


## -parameters




### -param dwlSpaceFreed [in]

Type: <b>DWORDLONG</b>

The amount of disk space, in bytes, that has been freed at this point in the purge. The disk cleanup manager uses this value to update its progress bar. 


### -param dwlSpaceToFree [in]

Type: <b>DWORDLONG</b>

The amount of disk space, in bytes, that remains to be freed at this point in the purge. 


### -param dwFlags [in]

Type: <b>DWORD</b>

A flag that can be sent to the disk cleanup manager. It can can have the following value: 



#### EVCCBF_LASTNOTIFICATION

This flag should be set if the handler will not call this method again. It is typically set when the purge is near completion. 


### -param pcwszStatus






#### - pwszReserved [in]

Type: <b>LPCWSTR</b>

Reserved. 


## -returns



Type: <b>HRESULT</b>

This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The handler should continue purging deletable files.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ABORT</b></dt>
</dl>
</td>
<td width="60%">
This value is returned when the user clicks the <b>Cancel</b> button on the disk cleanup manager's dialog box while a scan is in progress. The handler should stop purging files and shut down.

</td>
</tr>
</table>
 




## -remarks



This method is typically called by the handler's <a href="https://msdn.microsoft.com/c42430da-9d6a-42e9-bc4f-325d986c7c48">Purge</a> method while the handler is purging deletable files. Handlers should call <b>PurgeProgress</b> periodically to keep the user informed of progress, especially if the purge will take a long time. Calling this method frequently also allows the handler to shut down promptly if a user cancels a purge. 



