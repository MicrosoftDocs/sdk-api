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

# IUpdateDownloader::Download


## -description


Starts a synchronous download of the content files that are associated with the updates.


## -parameters




### -param retval [out]

An <a href="https://msdn.microsoft.com/293bea59-acec-4774-adb9-1ad1d29406c3">IDownloadResult</a> interface that contains result codes for the download.


## -returns



Returns <b>S_OK</b> if successful. Otherwise, returns a COM or Windows error code. 

This method can also return the following error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WU_E_INVALID_OPERATION</b></dt>
</dl>
</td>
<td width="60%">
The computer cannot access the update site.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WU_E_NO_UPDATE</b></dt>
</dl>
</td>
<td width="60%">
Windows Update Agent (WUA) does not have updates in the collection.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WU_E_NOT_INITIALIZED</b></dt>
</dl>
</td>
<td width="60%">
Windows Update Agent is not initialized.

</td>
</tr>
</table>
 




## -remarks



This method returns <b>WU_E_INVALID_OPERATION</b> if the object that is implementing the interface is locked down.

This method returns <b>WU_E_NO_UPDATE</b> if the <a href="https://msdn.microsoft.com/7c0444be-a9eb-461a-858e-1dea670afd06">Updates</a> property of the <a href="https://msdn.microsoft.com/8f9f3430-fc78-46cb-9dc8-b97e9d35d91c">IUpdateDownloader</a> interface is not set. This method also returns <b>WU_E_NO_UPDATE</b> if the <b>Updates</b> property is set to an empty collection.

This method returns <b>SUS_E_NOT_INITIALIZED</b> if the download job does not contain updates.




## -see-also




<a href="https://msdn.microsoft.com/8f9f3430-fc78-46cb-9dc8-b97e9d35d91c">IUpdateDownloader</a>
 

 

