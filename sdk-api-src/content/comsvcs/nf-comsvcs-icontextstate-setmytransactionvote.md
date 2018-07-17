---
UID: NF:comsvcs.IContextState.SetMyTransactionVote
title: IContextState::SetMyTransactionVote
author: windows-sdk-content
description: Sets the consistent flag.
old-location: cos\icontextstate_setmytransactionvote.htm
old-project: cossdk
ms.assetid: ec88f99a-cb24-42a9-8f2a-add7ddbec719
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: IContextState interface [COM+],SetMyTransactionVote method, IContextState.SetMyTransactionVote, IContextState::SetMyTransactionVote, SetMyTransactionVote, SetMyTransactionVote method [COM+], SetMyTransactionVote method [COM+],IContextState interface, _cos_IContextState_SetMyTransactionVote, comsvcs/IContextState::SetMyTransactionVote, cos.icontextstate_setmytransactionvote
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: TRACKING_COLL_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - IContextState.SetMyTransactionVote
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IContextState::SetMyTransactionVote


## -description


Sets the consistent flag.


## -parameters




### -param txVote [in]

The consistent flag. For a list of values, see the <a href="https://msdn.microsoft.com/2fea9ac5-f714-4682-a78c-bfe9396fccd5">TransactionVote</a> enumeration. Set this parameter to TxCommit if the consistent flag is true;set it to TxAbort if the consistent flag is false.


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

<a href="https://msdn.microsoft.com/47b23cae-d5fc-4788-ab1c-93d6d8ee3f01">Just-in-Time Activation</a> is not available to this context.

</td>
</tr>
</table>
 




## -remarks



COM+ inspects this flag only when deactivating the object, and the flag can be set multiple times within a method call.

The default value of the consistent flag is true.




## -see-also




<a href="https://msdn.microsoft.com/a641fa95-5587-4362-9869-e5c27c6dd2ce">Consistent and Done Flags</a>



<a href="https://msdn.microsoft.com/cba54ad7-c670-4efb-ad3b-aca1daabc4a3">IContextState</a>
 

 

