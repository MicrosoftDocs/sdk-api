---
UID: NN:comsvcs.IContextState
title: IContextState (comsvcs.h)
description: Controls object deactivation and transaction voting by manipulating context state flags.helpviewer_keywords: ["IContextState","IContextState interface [COM+]","IContextState interface [COM+]","described","_cos_IContextState","comsvcs/IContextState","cos.icontextstate"]
old-location: cos\icontextstate.htm
tech.root: cossdk
ms.assetid: cba54ad7-c670-4efb-ad3b-aca1daabc4a3
ms.date: 12/05/2018
ms.keywords: IContextState, IContextState interface [COM+], IContextState interface [COM+],described, _cos_IContextState, comsvcs/IContextState, cos.icontextstate
f1_keywords:
- comsvcs/IContextState
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- ComSvcs.h
api_name:
- IContextState
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IContextState interface


## -description


Controls object deactivation and transaction voting by manipulating context state flags. By calling the methods of this interface, you can set consistent and done flags independently of each other and get the current status of each flag. Also, the methods of this interface return errors that indicate the absence of just-in-time (JIT) activation or the absence of a transaction.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IContextState</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IContextState</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IContextState</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-icontextstate-getdeactivateonreturn">GetDeactivateOnReturn</a>
</td>
<td align="left" width="63%">
Retrieves the value of the done flag.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-icontextstate-getmytransactionvote">GetMyTransactionVote</a>
</td>
<td align="left" width="63%">
Retrieves the value of the consistent flag.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-icontextstate-setdeactivateonreturn">SetDeactivateOnReturn</a>
</td>
<td align="left" width="63%">
Sets the done flag, which controls whether the object deactivates on method return.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-icontextstate-setmytransactionvote">SetMyTransactionVote</a>
</td>
<td align="left" width="63%">
Sets the consistent flag.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/cossdk/consistent-and-done-flags">Consistent and Done Flags</a>
 

 

