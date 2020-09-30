---
UID: NF:comsvcs.IContextState.GetMyTransactionVote
title: IContextState::GetMyTransactionVote (comsvcs.h)
description: Retrieves the value of the consistent flag.
helpviewer_keywords: ["GetMyTransactionVote","GetMyTransactionVote method [COM+]","GetMyTransactionVote method [COM+]","IContextState interface","IContextState interface [COM+]","GetMyTransactionVote method","IContextState.GetMyTransactionVote","IContextState::GetMyTransactionVote","_cos_IContextState_GetMyTransactionVote","comsvcs/IContextState::GetMyTransactionVote","cos.icontextstate_getmytransactionvote"]
old-location: cos\icontextstate_getmytransactionvote.htm
tech.root: cos
ms.assetid: 72384c53-ce4a-413e-8ff6-33925c8cd0df
ms.date: 12/05/2018
ms.keywords: GetMyTransactionVote, GetMyTransactionVote method [COM+], GetMyTransactionVote method [COM+],IContextState interface, IContextState interface [COM+],GetMyTransactionVote method, IContextState.GetMyTransactionVote, IContextState::GetMyTransactionVote, _cos_IContextState_GetMyTransactionVote, comsvcs/IContextState::GetMyTransactionVote, cos.icontextstate_getmytransactionvote
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IContextState::GetMyTransactionVote
 - comsvcs/IContextState::GetMyTransactionVote
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - IContextState.GetMyTransactionVote
---

# IContextState::GetMyTransactionVote


## -description

Retrieves the value of the consistent flag. Retrieving this value before deactivating the object allows the object to confirm its vote.

## -parameters

### -param ptxVote [out]

The consistent flag. For a list of values, see the <a href="/windows/desktop/api/comsvcs/ne-comsvcs-transactionvote">TransactionVote</a> enumeration. This parameter is set to TxCommit if the consistent flag is true; it is set to TxAbort if the consistent flag is false.

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

<a href="/windows/desktop/cossdk/consistent-and-done-flags">Consistent and Done Flags</a>



<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icontextstate">IContextState</a>