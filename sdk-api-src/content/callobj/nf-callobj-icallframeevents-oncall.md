---
UID: NF:callobj.ICallFrameEvents.OnCall
title: ICallFrameEvents::OnCall (callobj.h)
description: Informs the event sink if it receives a method call on the interceptor. The sink is provided with an ICallFrame instance which is bound to the intercepted incoming method invocation. Through that sink the call frame can be manipulated in various ways.
helpviewer_keywords: ["ICallFrameEvents interface [COM]","OnCall method","ICallFrameEvents.OnCall","ICallFrameEvents::OnCall","OnCall","OnCall method [COM]","OnCall method [COM]","ICallFrameEvents interface","_com_icallframeevents_oncall","callobj/ICallFrameEvents::OnCall","com.icallframeevents_oncall"]
old-location: com\icallframeevents_oncall.htm
tech.root: com
ms.assetid: bdccc4a7-e408-4186-8cc0-b14feacfbf04
ms.date: 12/05/2018
ms.keywords: ICallFrameEvents interface [COM],OnCall method, ICallFrameEvents.OnCall, ICallFrameEvents::OnCall, OnCall, OnCall method [COM], OnCall method [COM],ICallFrameEvents interface, _com_icallframeevents_oncall, callobj/ICallFrameEvents::OnCall, com.icallframeevents_oncall
req.header: callobj.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Callobj.idl
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
 - ICallFrameEvents::OnCall
 - callobj/ICallFrameEvents::OnCall
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Callobj.h
api_name:
 - ICallFrameEvents.OnCall
---

# ICallFrameEvents::OnCall


## -description

Informs the event sink if it receives a method call on the interceptor. The sink is provided with an <a href="/windows/desktop/api/callobj/nn-callobj-icallframe">ICallFrame</a> instance which is bound to the intercepted incoming method invocation. Through that sink the call frame can be manipulated in various ways.

## -parameters

### -param pFrame [in]

A call frame bound to the just-received invocation.

## -returns

This method can return the following values.

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
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
An unexpected error has occurred.

</td>
</tr>
</table>

## -remarks

On return from <b>OnCall</b>, the interceptor assumes that by some means the out-values of the method have been appropriately initialized as needed, if any; the interceptor does not itself manipulate the call frame further in any way. Typically, the <b>OnCall</b> implementation will have set the out-values by some means, either by invoking the call frame on an object, successfully unmarshalling some previously marshaled out-values, or clearing them with <a href="/windows/desktop/api/callobj/nf-callobj-icallframe-free">ICallFrame::Free</a>.

The return value should also have been appropriately set during the call in a similar manner. See <a href="/windows/desktop/api/callobj/nf-callobj-icallframe-setreturnvalue">ICallFrame::SetReturnValue</a>.

## -see-also

<a href="/windows/desktop/api/callobj/nn-callobj-icallframe">ICallFrame</a>



<a href="/windows/desktop/api/callobj/nn-callobj-icallframeevents">ICallFrameEvents</a>