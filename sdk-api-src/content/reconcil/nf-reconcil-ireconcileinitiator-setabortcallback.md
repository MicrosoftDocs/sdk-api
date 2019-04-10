---
UID: NF:reconcil.IReconcileInitiator.SetAbortCallback
title: IReconcileInitiator::SetAbortCallback (reconcil.h)
author: windows-sdk-content
description: Sets the object through which the initiator can asynchronously terminate a reconciliation. A briefcase reconciler typically sets this object for reconciliations that are lengthy or involve user interaction.
old-location: lwef\ireconcileinitiator_setabortcallback.htm
tech.root: lwef
ms.assetid: 9c251e14-e080-480a-80c2-f3686429689f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IReconcileInitiator interface [Legacy Windows Environment Features],SetAbortCallback method, IReconcileInitiator.SetAbortCallback, IReconcileInitiator::SetAbortCallback, SetAbortCallback, SetAbortCallback method [Legacy Windows Environment Features], SetAbortCallback method [Legacy Windows Environment Features],IReconcileInitiator interface, _win32_IReconcileInitiator_SetAbortCallback, lwef.ireconcileinitiator_setabortcallback, reconcil/IReconcileInitiator::SetAbortCallback, shell.ireconcileinitiator_setabortcallback
ms.topic: method
req.header: reconcil.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
req.dll: Shell32.dll (version 4.0 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IReconcileInitiator.SetAbortCallback
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IReconcileInitiator::SetAbortCallback


## -description


Sets the object through which the initiator can asynchronously terminate a reconciliation. A briefcase reconciler typically sets this object for reconciliations that are lengthy or involve user interaction. 


## -parameters




### -param punkForAbort

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a>*</b>

The address of the <a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> interface for the object. The initiator signals a request to terminate the reconciliation by using the <a href="https://msdn.microsoft.com/en-us/library/ms682317(v=VS.85).aspx">IUnknown::Release</a> method to release the object. This parameter may be <b>NULL</b> to direct the initiator to remove the previously specified object. 


## -returns



Type: <b>HRESULT</b>

Returns the S_OK value if successful, or one of the following error values otherwise. 

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>REC_E_NOCALLBACK</b></dt>
</dl>
</td>
<td width="60%">
The initiator does not support termination of reconciliation operations and does not hold the specified object.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
Unspecified error.

</td>
</tr>
</table>
 




## -remarks



The initiator can accept or reject the object. If the initiator accepts the object, the briefcase reconciler must remove the object by calling this method with a <b>NULL</b> parameter when the reconciliation is complete. Because the reconciler removes the object after completing reconciliation, there may be times when the initiator releases the object after reconciliation is complete. In such cases, the reconciler ignores the request to terminate. 

If the reconciliation is terminated, the <a href="https://msdn.microsoft.com/6dfeb68e-fd23-4812-8a3c-ab27fc00a4ad">Reconcile</a> method must return either the REC_E_ABORTED or REC_E_NOTCOMPLETE value. 




## -see-also




<a href="https://msdn.microsoft.com/1a32d67f-1ddc-49dc-af88-b8c41a50ac54">IReconcileInitiator</a>
 

 

