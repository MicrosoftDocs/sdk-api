---
UID: NF:msinkaut.IInkDisp.CreateStrokes
title: IInkDisp::CreateStrokes (msinkaut.h)
description: Creates a new InkStrokes collection from existing IInkStrokeDisp objects.
helpviewer_keywords: ["21e68151-38c9-414f-840c-c2687a05aea4","CreateStrokes","CreateStrokes method [Tablet PC]","CreateStrokes method [Tablet PC]","IInkDisp interface","IInkDisp interface [Tablet PC]","CreateStrokes method","IInkDisp.CreateStrokes","IInkDisp::CreateStrokes","msinkaut/IInkDisp::CreateStrokes","tablet.inkdisp_createstrokes"]
old-location: tablet\inkdisp_createstrokes.htm
tech.root: tablet
ms.assetid: 21e68151-38c9-414f-840c-c2687a05aea4
ms.date: 12/05/2018
ms.keywords: 21e68151-38c9-414f-840c-c2687a05aea4, CreateStrokes, CreateStrokes method [Tablet PC], CreateStrokes method [Tablet PC],IInkDisp interface, IInkDisp interface [Tablet PC],CreateStrokes method, IInkDisp.CreateStrokes, IInkDisp::CreateStrokes, msinkaut/IInkDisp::CreateStrokes, tablet.inkdisp_createstrokes
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IInkDisp::CreateStrokes
 - msinkaut/IInkDisp::CreateStrokes
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - InkObj.dll
 - InkObj.dll.dll
api_name:
 - IInkDisp.CreateStrokes
---

# IInkDisp::CreateStrokes


## -description

Creates a new <a href="/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes</a> collection from existing <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp">IInkStrokeDisp</a> objects.

## -parameters

### -param StrokeIds [in, optional]

Optional. Specifies an array of stroke IDs that exist in the <a href="/windows/desktop/tablet/inkdisp-class">InkDisp</a> object. The strokes with these IDs are added to a new <a href="/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes</a> collection. The default value is <b>NULL</b>.

For more information about the VARIANT structure, see <a href="/windows/desktop/tablet/using-the-com-library">Using the COM Library</a>.

### -param Strokes [out, retval]

When this method returns, contains a pointer to a new <a href="/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes</a> collection.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid VARIANT type (only VT_ARRAY | VT_I4 supported).

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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Cannot allocate memory to create the new Strokes collection.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TPC_E_INVALID_STROKE</b></dt>
</dl>
</td>
<td width="60%">
Stroke IDs that do not exist were passed to the method.

</td>
</tr>
</table>

## -remarks

If the <i>ids</i> parameter is <b>NULL</b> or an empty array, then an empty <a href="/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes</a> collection is created.

## -see-also

<a href="../msinkaut/nn-msinkaut-iinkdisp.md">IInkDisp</a>



<a href="/windows/desktop/tablet/inkdisp-class">InkDisp Class</a>



<a href="/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes Collection</a>
