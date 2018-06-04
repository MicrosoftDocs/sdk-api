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

# IContextState::GetMyTransactionVote


## -description


Retrieves the value of the consistent flag. Retrieving this value before deactivating the object allows the object to confirm its vote.


## -parameters




### -param ptxVote [out]

The consistent flag. For a list of values, see the <a href="https://msdn.microsoft.com/2fea9ac5-f714-4682-a78c-bfe9396fccd5">TransactionVote</a> enumeration. This parameter is set to TxCommit if the consistent flag is true; it is set to TxAbort if the consistent flag is false.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, and E_FAIL, as well as the following values.

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
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CONTEXT_E_NOTRANSACTION</b></dt>
</dl>
</td>
<td width="60%">
The object is not running in a transaction.

</td>
</tr>
</table>
 




## -remarks



If the method fails, you may be able to determine that a transaction is not present, based on the <b>HRESULT</b> value. If the method succeeds, it returns a value based on the consistent flag. From this value, you can determine whether the object can be committed or must be aborted. Regardless of the object's state, the object must be participating in a transaction.




## -see-also




<a href="https://msdn.microsoft.com/a641fa95-5587-4362-9869-e5c27c6dd2ce">Consistent and Done Flags</a>



<a href="https://msdn.microsoft.com/cba54ad7-c670-4efb-ad3b-aca1daabc4a3">IContextState</a>
 

 

