---
UID: NF:comsvcs.ITransactionStatus.GetTransactionStatus
title: ITransactionStatus::GetTransactionStatus
author: windows-driver-content
description: Retrieves the transaction status.
old-location: cos\itransactionstatus_gettransactionstatus.htm
old-project: cossdk
ms.assetid: c8c37aee-c5d2-479f-989f-461877ee6136
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: GetTransactionStatus, GetTransactionStatus method [COM+], GetTransactionStatus method [COM+],ITransactionStatus interface, ITransactionStatus interface [COM+],GetTransactionStatus method, ITransactionStatus.GetTransactionStatus, ITransactionStatus::GetTransactionStatus, _cos_ITransactionStatus_GetTransactionStatus, comsvcs/ITransactionStatus::GetTransactionStatus, cos.itransactionstatus_gettransactionstatus
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: comsvcs.h
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
req.typenames: TRACKING_COLL_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	ComSvcs.h
api_name:
-	ITransactionStatus.GetTransactionStatus
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
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
 

 

