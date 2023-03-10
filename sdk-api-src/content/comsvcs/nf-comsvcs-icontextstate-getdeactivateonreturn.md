---
UID: NF:comsvcs.IContextState.GetDeactivateOnReturn
title: IContextState::GetDeactivateOnReturn (comsvcs.h)
description: Retrieves the value of the done flag.
helpviewer_keywords: ["GetDeactivateOnReturn","GetDeactivateOnReturn method [COM+]","GetDeactivateOnReturn method [COM+]","IContextState interface","IContextState interface [COM+]","GetDeactivateOnReturn method","IContextState.GetDeactivateOnReturn","IContextState::GetDeactivateOnReturn","_cos_IContextState_GetDeactivateOnReturn","comsvcs/IContextState::GetDeactivateOnReturn","cos.icontextstate_getdeactivateonreturn"]
old-location: cos\icontextstate_getdeactivateonreturn.htm
tech.root: cos
ms.assetid: 4e9623eb-1bf1-4649-9071-b731bf95a401
ms.date: 12/05/2018
ms.keywords: GetDeactivateOnReturn, GetDeactivateOnReturn method [COM+], GetDeactivateOnReturn method [COM+],IContextState interface, IContextState interface [COM+],GetDeactivateOnReturn method, IContextState.GetDeactivateOnReturn, IContextState::GetDeactivateOnReturn, _cos_IContextState_GetDeactivateOnReturn, comsvcs/IContextState::GetDeactivateOnReturn, cos.icontextstate_getdeactivateonreturn
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
 - IContextState::GetDeactivateOnReturn
 - comsvcs/IContextState::GetDeactivateOnReturn
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
 - IContextState.GetDeactivateOnReturn
---

# IContextState::GetDeactivateOnReturn


## -description

Retrieves the value of the done flag.

## -parameters

### -param pbDeactivate [out]

The done flag.

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

When <i>pbDeactivate</i> is <b>FALSE</b> for the root object of a transaction, the object does not deactivate and the transaction does not terminate unless the client releases its reference to the object or until the done flag is set to <b>TRUE</b>.

## -see-also

<a href="/windows/desktop/cossdk/consistent-and-done-flags">Consistent and Done Flags</a>



<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icontextstate">IContextState</a>