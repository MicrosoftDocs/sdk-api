---
UID: NF:callobj.ICallFrame.Invoke
title: ICallFrame::Invoke
author: windows-sdk-content
description: Applies this activation record to an object. In a marshalling situation, typically this is carried out on the server side, and is the means by which the work of the actual object is accomplished.
old-location: com\icallframe_invoke.htm
old-project: com
ms.assetid: 75cb7b96-55c9-4aee-b507-a549e2af38bc
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ICallFrame interface [COM],Invoke method, ICallFrame.Invoke, ICallFrame::Invoke, Invoke, Invoke method [COM], Invoke method [COM],ICallFrame interface, _com_icallframe_invoke, callobj/ICallFrame::Invoke, com.icallframe_invoke
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: CALLFRAME_COPY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Callobj.h
api_name:
 - ICallFrame.Invoke
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ICallFrame::Invoke


## -description


Applies this activation record to an object.
In a marshalling situation, typically this is carried out on the server side, and is the means by which the work of the actual object is accomplished.


## -parameters




### -param pvReceiver [in]

The interface on which the invocation is to occur. The caller is responsible for ensuring that this interface is of the appropriate IID; the implementation will simply do a cast and assume that is the case.


### -param param






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



Generally speaking, carrying out the invocation involves allocating a new stack frame, shallow-copying down the data in the original frame, then calling the appropriate method in the indicated object. The object invoked may then choose to modify [out] parameters, which are reachable from the copied frame, according to the appropriate semantics of the invocation. When the invocation returns from the object, the call frame automatically captures the return value from <a href="https://msdn.microsoft.com/848cccc7-19c8-4ce6-b609-bcf798ec8c76">ICallFrame::SetReturnValue</a>.




## -see-also




<a href="https://msdn.microsoft.com/56a75123-f402-4187-af13-d31f72a5f094">ICallFrame</a>
 

 

