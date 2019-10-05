---
UID: NF:msinkaut.IInkStrokes.RemoveStrokes
title: IInkStrokes::RemoveStrokes (msinkaut.h)
author: windows-sdk-content
description: Removes strokes from the collection.
old-location: tablet\inkstrokes_removestrokes.htm
tech.root: tablet
ms.assetid: 6f90d175-747c-4bf5-978a-286b69bf068a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 6f90d175-747c-4bf5-978a-286b69bf068a, IInkStrokes interface [Tablet PC],RemoveStrokes method, IInkStrokes.RemoveStrokes, IInkStrokes::RemoveStrokes, RemoveStrokes, RemoveStrokes method [Tablet PC], RemoveStrokes method [Tablet PC],IInkStrokes interface, msinkaut/IInkStrokes::RemoveStrokes, tablet.inkstrokes_removestrokes
ms.topic: method
f1_keywords: 
 - "msinkaut/IInkStrokes.RemoveStrokes"
dev_langs:
 - c++
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
 - IInkStrokes.RemoveStrokes
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IInkStrokes::RemoveStrokes


## -description



Removes strokes from the collection.




## -parameters




### -param InkStrokes [in]

The strokes to remove from the collection.


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
Cannot allocate Stroke handler helper object.

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
IInkStrokes* does not point to a valid <a href="https://docs.microsoft.com/windows/desktop/tablet/inkdisp-class">InkDisp</a> object.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INK_MISMATCHED_INK_OBJECT</b></dt>
</dl>
</td>
<td width="60%">
The <a href="https://docs.microsoft.com/windows/desktop/tablet/inkdisp-class">InkDisp</a> object of the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes</a> collection and the specified InkStrokes don't match.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
Unexpected parameter or property type.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Mt846806(v=VS.85).aspx">IInkStrokes</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes Collection</a>



<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokes-remove">Remove Method [InkStrokes Collection]</a>
 

 

