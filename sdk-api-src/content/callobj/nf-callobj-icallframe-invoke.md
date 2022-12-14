---
UID: NF:callobj.ICallFrame.Invoke
title: ICallFrame::Invoke (callobj.h)
description: Applies this activation record to an object. In a marshalling situation, typically this is carried out on the server side, and is the means by which the work of the actual object is accomplished.
helpviewer_keywords: ["ICallFrame interface [COM]","Invoke method","ICallFrame.Invoke","ICallFrame::Invoke","Invoke","Invoke method [COM]","Invoke method [COM]","ICallFrame interface","_com_icallframe_invoke","callobj/ICallFrame::Invoke","com.icallframe_invoke"]
old-location: com\icallframe_invoke.htm
tech.root: com
ms.assetid: 75cb7b96-55c9-4aee-b507-a549e2af38bc
ms.date: 12/05/2018
ms.keywords: ICallFrame interface [COM],Invoke method, ICallFrame.Invoke, ICallFrame::Invoke, Invoke, Invoke method [COM], Invoke method [COM],ICallFrame interface, _com_icallframe_invoke, callobj/ICallFrame::Invoke, com.icallframe_invoke
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
 - ICallFrame::Invoke
 - callobj/ICallFrame::Invoke
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
 - ICallFrame.Invoke
---

# ICallFrame::Invoke


## -description

Applies this activation record to an object.
In a marshalling situation, typically this is carried out on the server side, and is the means by which the work of the actual object is accomplished.

## -parameters

### -param pvReceiver [in]

The interface on which the invocation is to occur. The caller is responsible for ensuring that this interface is of the appropriate IID; the implementation will simply do a cast and assume that is the case.

### -param ...

Additional parameters.

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
<dt><b>CALLFRAME_E_ALREADYINVOKED</b></dt>
</dl>
</td>
<td width="60%">
An invocation has already been made from this frame.

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

Generally speaking, carrying out the invocation involves allocating a new stack frame, shallow-copying down the data in the original frame, then calling the appropriate method in the indicated object. The object invoked may then choose to modify [out] parameters, which are reachable from the copied frame, according to the appropriate semantics of the invocation. When the invocation returns from the object, the call frame automatically captures the return value from <a href="/windows/desktop/api/callobj/nf-callobj-icallframe-setreturnvalue">ICallFrame::SetReturnValue</a>.

## -see-also

<a href="/windows/desktop/api/callobj/nn-callobj-icallframe">ICallFrame</a>

