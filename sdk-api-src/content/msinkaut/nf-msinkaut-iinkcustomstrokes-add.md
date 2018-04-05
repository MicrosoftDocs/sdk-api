---
UID: NF:msinkaut.IInkCustomStrokes.Add
title: IInkCustomStrokes::Add method
author: windows-driver-content
description: Adds an InkStrokes collection to an IInkCustomStrokes collection.
old-location: tablet\iinkcustomstrokes_add.htm
old-project: tablet
ms.assetid: 482906b2-131e-4baa-8ed7-c11f79f05e4b
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: 482906b2-131e-4baa-8ed7-c11f79f05e4b, Add method [Tablet PC], Add method [Tablet PC], IInkCustomStrokes interface, Add,IInkCustomStrokes.Add, IInkCustomStrokes, IInkCustomStrokes interface [Tablet PC], Add method, IInkCustomStrokes::Add, msinkaut/IInkCustomStrokes::Add, tablet.iinkcustomstrokes_add
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: TabletPropertyMetricUnit
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	InkObj.dll
-	InkObj.dll.dll
api_name:
-	IInkCustomStrokes.Add
product: Windows
targetos: Windows
req.lib: InkObj.dll
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IInkCustomStrokes::Add method


## -description



Adds an <a href="https://msdn.microsoft.com/c7fb921c-0bd2-48aa-b092-ab1fb08c0697">InkStrokes</a> collection to an <a href="https://msdn.microsoft.com/0b4eb5d6-ccf0-46c1-ae02-a393e67b817e">IInkCustomStrokes</a> collection.




## -parameters




### -param Name [in]

Specifies the name of the <a href="https://msdn.microsoft.com/c7fb921c-0bd2-48aa-b092-ab1fb08c0697">InkStrokes</a> collection to add to the <a href="https://msdn.microsoft.com/0b4eb5d6-ccf0-46c1-ae02-a393e67b817e">IInkCustomStrokes</a> collection.

For more information about the BSTR data type, see <a href="https://msdn.microsoft.com/fa43fad9-804c-42d9-9717-6686d5f98ed8">Using the COM Library</a>.


### -param Strokes [in]

Specifies the <a href="https://msdn.microsoft.com/c7fb921c-0bd2-48aa-b092-ab1fb08c0697">InkStrokes</a> collection to add to the <a href="https://msdn.microsoft.com/0b4eb5d6-ccf0-46c1-ae02-a393e67b817e">IInkCustomStrokes</a> collection.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The item already exists in the collection or a parameter contained an invalid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Cannot allocate memory to complete the operation.

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
The collection of strokes is incompatible with the API.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INK_MISMATCHED_INK_OBJECT</b></dt>
</dl>
</td>
<td width="60%">
The strokes parameter is associated with a different INK object.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/0b4eb5d6-ccf0-46c1-ae02-a393e67b817e">IInkCustomStrokes Interface</a>



<a href="https://msdn.microsoft.com/c7fb921c-0bd2-48aa-b092-ab1fb08c0697">InkStrokes Collection</a>
 

 

