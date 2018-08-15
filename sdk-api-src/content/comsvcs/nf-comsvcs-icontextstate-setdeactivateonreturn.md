---
UID: NF:comsvcs.IContextState.SetDeactivateOnReturn
title: IContextState::SetDeactivateOnReturn
author: windows-sdk-content
description: Sets the done flag, which controls whether the object deactivates on method return.
old-location: cos\icontextstate_setdeactivateonreturn.htm
old-project: cossdk
ms.assetid: 29dfeb6f-1961-4d6f-b5c4-fcd0eb4a7bec
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IContextState interface [COM+],SetDeactivateOnReturn method, IContextState.SetDeactivateOnReturn, IContextState::SetDeactivateOnReturn, SetDeactivateOnReturn, SetDeactivateOnReturn method [COM+], SetDeactivateOnReturn method [COM+],IContextState interface, _cos_IContextState_SetDeactivateOnReturn, comsvcs/IContextState::SetDeactivateOnReturn, cos.icontextstate_setdeactivateonreturn
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: comsvcs.h
req.include-header: 
req.redist: 
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
 - IContextState.SetDeactivateOnReturn
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
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

<a href="https://msdn.microsoft.com/47b23cae-d5fc-4788-ab1c-93d6d8ee3f01">Just-in-Time Activation</a> is not available to this context.

</td>
</tr>
</table>
 




## -remarks



When set to true, the done flag causes the object to deactivate when the method call returns. When set to false, the object remains active after the method call returns.
The default value of the done flag is false.




## -see-also




<a href="https://msdn.microsoft.com/a641fa95-5587-4362-9869-e5c27c6dd2ce">Consistent and Done Flags</a>



<a href="https://msdn.microsoft.com/cba54ad7-c670-4efb-ad3b-aca1daabc4a3">IContextState</a>
 

 

