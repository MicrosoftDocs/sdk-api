---
UID: NF:msinkaut.IInkDisp.ExtractWithRectangle
title: IInkDisp::ExtractWithRectangle (msinkaut.h)
description: Cuts or copies strokes from an existing InkDisp object and pastes them into a new InkDisp object, by using the known rectangle to determine which strokes to extract.
helpviewer_keywords: ["ExtractWithRectangle","ExtractWithRectangle method [Tablet PC]","ExtractWithRectangle method [Tablet PC]","IInkDisp interface","IInkDisp interface [Tablet PC]","ExtractWithRectangle method","IInkDisp.ExtractWithRectangle","IInkDisp::ExtractWithRectangle","b32467a8-a677-4a80-8029-d364e6e372c6","msinkaut/IInkDisp::ExtractWithRectangle","tablet.inkdisp_extractwithrectangle"]
old-location: tablet\inkdisp_extractwithrectangle.htm
tech.root: tablet
ms.assetid: b32467a8-a677-4a80-8029-d364e6e372c6
ms.date: 12/05/2018
ms.keywords: ExtractWithRectangle, ExtractWithRectangle method [Tablet PC], ExtractWithRectangle method [Tablet PC],IInkDisp interface, IInkDisp interface [Tablet PC],ExtractWithRectangle method, IInkDisp.ExtractWithRectangle, IInkDisp::ExtractWithRectangle, b32467a8-a677-4a80-8029-d364e6e372c6, msinkaut/IInkDisp::ExtractWithRectangle, tablet.inkdisp_extractwithrectangle
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
 - IInkDisp::ExtractWithRectangle
 - msinkaut/IInkDisp::ExtractWithRectangle
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
 - IInkDisp.ExtractWithRectangle
---

# IInkDisp::ExtractWithRectangle


## -description

Cuts or copies strokes from an existing <a href="/windows/desktop/tablet/inkdisp-class">InkDisp</a> object and pastes them into a new <b>InkDisp</b> object, by using the known rectangle to determine which strokes to extract.

## -parameters

### -param Rectangle [in]

Specifies the <a href="/windows/desktop/tablet/inkrectangle-class">InkRectangle</a> object which delimits the ink to extract from the <a href="/windows/desktop/tablet/inkdisp-class">InkDisp</a> object.

### -param extractFlags [in, optional]

Optional. Specifies the <a href="/windows/desktop/api/msinkaut/ne-msinkaut-inkextractflags">InkExtractFlags</a> enumeration type, which determines whether the ink should be cut or copied from the existing <a href="/windows/desktop/tablet/inkdisp-class">InkDisp</a> object. The default value is IEF_DEFAULT, which cuts the strokes from the existing <b>InkDisp</b> object.

### -param ExtractedInk [out, retval]

When this method returns, contains a pointer to an <a href="/windows/desktop/tablet/inkdisp-class">InkDisp</a> object that contains the extracted collection of strokes.

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
<dt><b>E_INK_SOME_STROKES_NOT_EXTRACTED</b></dt>
</dl>
</td>
<td width="60%">
Not all strokes were extracted.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid extraction flags.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>REGDB_CLASSNOTREG</b></dt>
</dl>
</td>
<td width="60%">
The Ink object was not registered.

</td>
</tr>
</table>

## -remarks

The new <a href="/windows/desktop/tablet/inkdisp-class">InkDisp</a> object retains the drawing attributes, properties, and coordinates of the original <b>InkDisp</b> object.

This method is useful for creating a new <a href="/windows/desktop/tablet/inkdisp-class">InkDisp</a> object without the deleted or cut strokes from the original object.

To extract strokes from a known collection of strokes, call the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-extractstrokes">ExtractStrokes Method</a>.

Only the portion of a stroke that is within the rectangle is added to the new <a href="/windows/desktop/tablet/inkdisp-class">InkDisp</a> object.

When the <i>extractFlags</i> parameter is <a href="/windows/desktop/api/msinkaut/ne-msinkaut-inkextractflags">RemoveFromOriginal</a> or <b>Default</b>, any strokes that cross the rectangle are split and the portion within the rectangle removed from the existing <a href="/windows/desktop/tablet/inkdisp-class">InkDisp</a> object.

## -see-also

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-extractstrokes">ExtractStrokes Method</a>



<a href="../msinkaut/nn-msinkaut-iinkdisp.md">IInkDisp</a>



<a href="/windows/desktop/tablet/inkdisp-class">InkDisp Class</a>



<a href="/windows/desktop/api/msinkaut/ne-msinkaut-inkextractflags">InkExtractFlags Enumeration</a>



<a href="/windows/desktop/tablet/inkrectangle-class">InkRectangle Class</a>



<a href="/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes Collection</a>
