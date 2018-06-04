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

# IBackgroundCopyJobHttpOptions::GetCustomHeaders


## -description


Retrieves the custom headers set by an earlier call to<a href="https://msdn.microsoft.com/422a331d-5b6b-48ec-b040-43a88be43ac3"> IBackgroundCopyJobHttpOptions::SetCustomHeaders</a> (that is, headers which BITS will be sending to the remote, not headers which BITS receives from the remote).


## -parameters




### -param pRequestHeaders [out]

Null-terminated string that contains the custom headers. Each header is terminated by a carriage return and line feed (CR/LF) character. To free the string when finished, call  the 
<a href="https://msdn.microsoft.com/en-us/library/windows/desktop/ms680722">CoTaskMemFree</a> function.


## -returns



The following table lists some of the possible return values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>S_OK</b></b></dt>
</dl>
</td>
<td width="60%">
Successfully retrieved the headers.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>S_FALSE</b></b></dt>
</dl>
</td>
<td width="60%">
The job does not specify custom headers.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>E_ACCESSDENIED</b></b></dt>
</dl>
</td>
<td width="60%">
The user does not have permission to retrieve the custom headers.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>RPC_X_NULL_REF_POINTER</b></b></dt>
</dl>
</td>
<td width="60%">
The <i>pRequestHeaders</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



Only the job owner can retrieve the custom headers. To specify the headers, call the <a href="https://msdn.microsoft.com/422a331d-5b6b-48ec-b040-43a88be43ac3">IBackgroundCopyJobHttpOptions::SetCustomHeaders</a> method.




## -see-also




<a href="https://msdn.microsoft.com/d8ccf65d-a4f1-44d9-9903-43e5529f1f29">IBackgroundCopyJobHttpOptions</a>



<a href="https://msdn.microsoft.com/422a331d-5b6b-48ec-b040-43a88be43ac3">IBackgroundCopyJobHttpOptions::SetCustomHeaders</a>
 

 

