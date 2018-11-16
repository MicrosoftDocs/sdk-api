---
UID: NF:comsvcs.IContextState.GetDeactivateOnReturn
title: IContextState::GetDeactivateOnReturn
author: windows-sdk-content
description: Retrieves the value of the done flag.
old-location: cos\icontextstate_getdeactivateonreturn.htm
tech.root: cossdk
ms.assetid: 4e9623eb-1bf1-4649-9071-b731bf95a401
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetDeactivateOnReturn, GetDeactivateOnReturn method [COM+], GetDeactivateOnReturn method [COM+],IContextState interface, IContextState interface [COM+],GetDeactivateOnReturn method, IContextState.GetDeactivateOnReturn, IContextState::GetDeactivateOnReturn, _cos_IContextState_GetDeactivateOnReturn, comsvcs/IContextState::GetDeactivateOnReturn, cos.icontextstate_getdeactivateonreturn
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IContextState.GetDeactivateOnReturn
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- comsvcs.h
: 
- IContextState.GetDeactivateOnReturn
: 
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

<a href="https://msdn.microsoft.com/47b23cae-d5fc-4788-ab1c-93d6d8ee3f01">Just-in-Time Activation</a> is not available to this context.

</td>
</tr>
</table>
 




## -remarks



When <i>pbDeactivate</i> is <b>FALSE</b> for the root object of a transaction, the object does not deactivate and the transaction does not terminate unless the client releases its reference to the object or until the done flag is set to <b>TRUE</b>.




## -see-also




<a href="https://msdn.microsoft.com/a641fa95-5587-4362-9869-e5c27c6dd2ce">Consistent and Done Flags</a>



<a href="https://msdn.microsoft.com/cba54ad7-c670-4efb-ad3b-aca1daabc4a3">IContextState</a>
 

 

