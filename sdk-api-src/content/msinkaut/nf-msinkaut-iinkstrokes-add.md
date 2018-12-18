---
UID: NF:msinkaut.IInkStrokes.Add
title: IInkStrokes::Add
author: windows-sdk-content
description: Adds an IInkStrokeDisp object or InkStrokes collection to an existing InkStrokes collection.
old-location: tablet\inkstrokes_add.htm
tech.root: tablet
ms.assetid: 5ea0932a-ba21-4c6a-a3bc-c122b5805e86
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: 5ea0932a-ba21-4c6a-a3bc-c122b5805e86, Add, Add method [Tablet PC], Add method [Tablet PC],IInkStrokes interface, IInkStrokes interface [Tablet PC],Add method, IInkStrokes.Add, IInkStrokes::Add, msinkaut/IInkStrokes::Add, tablet.inkstrokes_add
ms.topic: method
req.header: msinkaut.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP Tablet PC Edition [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: InkObj.dll
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - InkObj.dll
 - InkObj.dll.dll
api_name:
 - IInkStrokes.Add
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IInkStrokes::Add


## -description



Adds an <a href="https://msdn.microsoft.com/b18464ba-feb6-4bb5-9fcf-82feff9bcce4">IInkStrokeDisp</a> object or <a href="https://msdn.microsoft.com/c7fb921c-0bd2-48aa-b092-ab1fb08c0697">InkStrokes</a> collection to an existing InkStrokes collection.




## -parameters




### -param InkStroke [in]

 The stroke to add to the <a href="https://msdn.microsoft.com/c7fb921c-0bd2-48aa-b092-ab1fb08c0697">InkStrokes</a> collection.


## -returns



This method can return one of these values.

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
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
A parameter contained an invalid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Cannot allocate <a href="https://msdn.microsoft.com/eaa89dfe-6141-4205-845b-634321130e26">Stroke</a> handler helper object.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INK_EXCEPTION</b></dt>
</dl>
</td>
<td width="60%">
An exception occurred inside the method.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INK_INCOMPATIBLE_OBJECT</b></dt>
</dl>
</td>
<td width="60%">
IInkStrokeDisp* does not point to a compatible <a href="https://msdn.microsoft.com/b18464ba-feb6-4bb5-9fcf-82feff9bcce4">IInkStrokeDisp</a> object.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INK_MISMATCHED_INK_OBJECT</b></dt>
</dl>
</td>
<td width="60%">
The <a href="https://msdn.microsoft.com/f942d6a3-f303-49df-a128-de9760b508ef">InkDisp</a> object of the <a href="https://msdn.microsoft.com/b18464ba-feb6-4bb5-9fcf-82feff9bcce4">IInkStrokeDisp</a> being added does not match the <b>InkDisp</b> object of the <a href="https://msdn.microsoft.com/c7fb921c-0bd2-48aa-b092-ab1fb08c0697">InkStrokes</a> collection.

</td>
</tr>
</table>
 




## -remarks



<div class="alert"><b>Note</b>  The stroke must already exist within the <a href="https://msdn.microsoft.com/f942d6a3-f303-49df-a128-de9760b508ef">InkDisp</a> object, and cannot belong to another <b>InkDisp</b> object. Also, this method does not copy or otherwise alter the <b>InkDisp</b> object, but merely adds this stroke to the collection.</div>
<div> </div>
Use this method to add one stroke to an <a href="https://msdn.microsoft.com/c7fb921c-0bd2-48aa-b092-ab1fb08c0697">InkStrokes</a> collection. To add one collection of strokes to another, use the <a href="https://msdn.microsoft.com/76580828-c776-4787-843c-db0acb768321">AddStrokes</a> method.




## -see-also




<a href="https://msdn.microsoft.com/76580828-c776-4787-843c-db0acb768321">AddStrokes Method</a>



<a href="https://msdn.microsoft.com/b18464ba-feb6-4bb5-9fcf-82feff9bcce4">IInkStrokeDisp Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Mt846806(v=VS.85).aspx">IInkStrokes</a>



<a href="https://msdn.microsoft.com/c7fb921c-0bd2-48aa-b092-ab1fb08c0697">InkStrokes Collection</a>
 

 

