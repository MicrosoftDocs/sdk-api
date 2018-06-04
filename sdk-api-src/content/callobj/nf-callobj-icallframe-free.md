---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# ICallFrame::Free


## -description


Frees the frame copy to avoid a memory leak.

When a copy of a call frame is made with the <a href="https://msdn.microsoft.com/library/windows/hardware/ff544217">Copy</a> method, the call frame does not clean up the copied data automatically. Therefore, after a copy of the call frame is returned, the user is responsible for calling the <b>Free</b> method to free the frame copy and avoid a memory leak.


## -parameters




### -param pframeArgsDest [in]

A pointer to an instance of the <a href="https://msdn.microsoft.com/56a75123-f402-4187-af13-d31f72a5f094">ICallFrame</a> interface. Represents the stack pointer of the call frame to which the out parameters should be copied before the frame copy is freed. The destination frame is usually the parent frame from which the frame was originally copied. This parameter is optional.

When freeing a frame and specifying a <i>pframeArgsDest</i> parameter which is in the same memory space as that of the receiver frame, then only the <i>pWalkerCopy</i> parameter is called on each interface pointer.


### -param pWalkerDestFree [in]

A pointer to an instance of the <a href="https://msdn.microsoft.com/1eeb00a3-d3c5-46f0-95a8-f694f802894b">ICallFrameWalker</a> interface. If there exist in and out parameters in <i>pframeArgsDest</i>, then the propagation requires that those values be freed. By providing the <i>pWalkerDestFree</i> object, interface pointers will be freed. If <i>pframeArgsDest</i> is <b>NULL</b>, then this parameter must also be <b>NULL</b> and the interface pointers should be released by calling the <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">Release</a> method.


### -param pWalkerCopy [in]

A pointer to an instance of the <a href="https://msdn.microsoft.com/1eeb00a3-d3c5-46f0-95a8-f694f802894b">ICallFrameWalker</a> interface. When the in and out parameters in <i>pframeArgsDest</i> are freed, then the propagation of out parameters is carried out. If this parameter is not specified, then the interface pointers will be passed to <a href="https://msdn.microsoft.com/b4316efd-73d4-4995-b898-8025a316ba63">AddRef</a>. This parameter is optional.


### -param freeFlags [in]

Flags from the <a href="https://msdn.microsoft.com/6a048133-7a89-4b55-afd3-5eb722d41914">CALLFRAME_FREE</a> enumeration.


### -param pWalkerFree [in]

A pointer to an instance of the <a href="https://msdn.microsoft.com/1eeb00a3-d3c5-46f0-95a8-f694f802894b">ICallFrameWalker</a> interface. When specified, a callback is made for each interface pointer encountered while freeing occurs. If this parameter is not specified, then the interface pointers are freed by the <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">Release</a> method.


### -param nullFlags [in]

Flags from the <a href="https://msdn.microsoft.com/99d83bdc-a33b-4233-84c6-350274f42965">CALLFRAME_NULL</a> enumeration.


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
 




## -see-also




<a href="https://msdn.microsoft.com/56a75123-f402-4187-af13-d31f72a5f094">ICallFrame</a>
 

 

