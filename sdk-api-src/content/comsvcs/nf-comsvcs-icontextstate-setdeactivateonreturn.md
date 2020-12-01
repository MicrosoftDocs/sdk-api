---
UID: NF:comsvcs.IContextState.SetDeactivateOnReturn
title: IContextState::SetDeactivateOnReturn (comsvcs.h)
description: Sets the done flag, which controls whether the object deactivates on method return.
helpviewer_keywords: ["IContextState interface [COM+]","SetDeactivateOnReturn method","IContextState.SetDeactivateOnReturn","IContextState::SetDeactivateOnReturn","SetDeactivateOnReturn","SetDeactivateOnReturn method [COM+]","SetDeactivateOnReturn method [COM+]","IContextState interface","_cos_IContextState_SetDeactivateOnReturn","comsvcs/IContextState::SetDeactivateOnReturn","cos.icontextstate_setdeactivateonreturn"]
old-location: cos\icontextstate_setdeactivateonreturn.htm
tech.root: cos
ms.assetid: 29dfeb6f-1961-4d6f-b5c4-fcd0eb4a7bec
ms.date: 12/05/2018
ms.keywords: IContextState interface [COM+],SetDeactivateOnReturn method, IContextState.SetDeactivateOnReturn, IContextState::SetDeactivateOnReturn, SetDeactivateOnReturn, SetDeactivateOnReturn method [COM+], SetDeactivateOnReturn method [COM+],IContextState interface, _cos_IContextState_SetDeactivateOnReturn, comsvcs/IContextState::SetDeactivateOnReturn, cos.icontextstate_setdeactivateonreturn
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
 - IContextState::SetDeactivateOnReturn
 - comsvcs/IContextState::SetDeactivateOnReturn
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
 - IContextState.SetDeactivateOnReturn
---

# IContextState::SetDeactivateOnReturn


## -description

Sets the done flag, which controls whether the object deactivates on method return.

## -parameters

### -param bDeactivate [in]

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

When set to true, the done flag causes the object to deactivate when the method call returns. When set to false, the object remains active after the method call returns.
The default value of the done flag is false.

## -see-also

<a href="/windows/desktop/cossdk/consistent-and-done-flags">Consistent and Done Flags</a>



<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icontextstate">IContextState</a>