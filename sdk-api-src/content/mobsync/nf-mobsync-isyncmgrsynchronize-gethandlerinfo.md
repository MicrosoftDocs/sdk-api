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

# ISyncMgrSynchronize::GetHandlerInfo


## -description


Obtains handler information.


## -parameters




### -param ppSyncMgrHandlerInfo [out]

Type: <b><a href="https://msdn.microsoft.com/8640796c-e5d0-48c8-b82b-7a153201e7de">SYNCMGRHANDLERINFO</a>**</b>

A pointer to a <a href="https://msdn.microsoft.com/8640796c-e5d0-48c8-b82b-7a153201e7de">SYNCMGRHANDLERINFO</a> structure.


## -returns



Type: <b>HRESULT</b>

This method supports the standard return values E_INVALIDARG, E_UNEXPECTED, and E_OUTOFMEMORY, and the following:

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
Handler information is returned successfully.

</td>
</tr>
</table>
 




## -remarks



The handler should use the <a href="https://msdn.microsoft.com/c4cb588d-9482-4f90-a92e-75b604540d5c">CoTaskMemAlloc</a> function to allocate memory.




## -see-also




<a href="https://msdn.microsoft.com/bb821672-10b1-4fe6-a752-6cd1ccd1e49e">ISyncMgrSynchronize</a>



<a href="https://msdn.microsoft.com/8640796c-e5d0-48c8-b82b-7a153201e7de">SYNCMGRHANDLERINFO</a>
 

 

