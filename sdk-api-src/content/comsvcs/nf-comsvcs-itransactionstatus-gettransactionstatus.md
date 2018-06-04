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

# ITransactionStatus::GetTransactionStatus


## -description


Retrieves the transaction status.


## -parameters




### -param pHrStatus [out]

he status of the transaction. See Remarks section for more information.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_FAIL, and S_OK.




## -remarks



The <i>pHrStatus</i> parameter is a pointer to an <b>HRESULT</b> value that indicates the transaction status according to the following table.

<table>
<tr>
<th>Value</th>
<th>Transaction status</th>
</tr>
<tr>
<td>S_OK
</td>
<td>The transaction has committed.
</td>
</tr>
<tr>
<td>XACT_S_LOCALLY_OK
</td>
<td>The transaction has neither committed nor aborted.
</td>
</tr>
<tr>
<td>XACT_E_NOTRANSACTION
</td>
<td>No transactions were being used through <a href="https://msdn.microsoft.com/84640b3b-1f43-4bec-abf6-c295cfb3da8b">CoEnterServiceDomain</a>.
</td>
</tr>
<tr>
<td>XACT_E_ABORTING
</td>
<td>The transaction is doomed and will eventually abort.
</td>
</tr>
<tr>
<td>XACT_E_ABORTED
</td>
<td>The transaction was aborted.
</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/df5eba93-6db7-478c-b6d7-831c20398d66">ITransactionStatus</a>
 

 

