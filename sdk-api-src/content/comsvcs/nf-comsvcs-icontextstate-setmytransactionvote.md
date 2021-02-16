---
UID: NF:comsvcs.IContextState.SetMyTransactionVote
title: IContextState::SetMyTransactionVote (comsvcs.h)
description: Sets the consistent flag.
helpviewer_keywords: ["IContextState interface [COM+]","SetMyTransactionVote method","IContextState.SetMyTransactionVote","IContextState::SetMyTransactionVote","SetMyTransactionVote","SetMyTransactionVote method [COM+]","SetMyTransactionVote method [COM+]","IContextState interface","_cos_IContextState_SetMyTransactionVote","comsvcs/IContextState::SetMyTransactionVote","cos.icontextstate_setmytransactionvote"]
old-location: cos\icontextstate_setmytransactionvote.htm
tech.root: cos
ms.assetid: ec88f99a-cb24-42a9-8f2a-add7ddbec719
ms.date: 12/05/2018
ms.keywords: IContextState interface [COM+],SetMyTransactionVote method, IContextState.SetMyTransactionVote, IContextState::SetMyTransactionVote, SetMyTransactionVote, SetMyTransactionVote method [COM+], SetMyTransactionVote method [COM+],IContextState interface, _cos_IContextState_SetMyTransactionVote, comsvcs/IContextState::SetMyTransactionVote, cos.icontextstate_setmytransactionvote
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
 - IContextState::SetMyTransactionVote
 - comsvcs/IContextState::SetMyTransactionVote
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
 - IContextState.SetMyTransactionVote
---

# IContextState::SetMyTransactionVote


## -description

Sets the consistent flag.

## -parameters

### -param txVote [in]

The consistent flag. For a list of values, see the <a href="/windows/desktop/api/comsvcs/ne-comsvcs-transactionvote">TransactionVote</a> enumeration. Set this parameter to TxCommit if the consistent flag is true;set it to TxAbort if the consistent flag is false.

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
<dt><b>CONTEXT_E_NOJIT</b></dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/cossdk/com--just-in-time-activation">Just-in-Time Activation</a> is not available to this context.

</td>
</tr>
</table>

## -remarks

COM+ inspects this flag only when deactivating the object, and the flag can be set multiple times within a method call.

The default value of the consistent flag is true.

## -see-also

<a href="/windows/desktop/cossdk/consistent-and-done-flags">Consistent and Done Flags</a>



<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icontextstate">IContextState</a>