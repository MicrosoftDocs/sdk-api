---
UID: NF:msinkaut.IInkDisp.ExtractStrokes
title: IInkDisp::ExtractStrokes (msinkaut.h)
description: Specifies the strokes to extract from an InkDisp Class and cut or copy into a new InkDisp Class, by using the known collection of strokes to determine which strokes to extract.
helpviewer_keywords: ["1cb109e5-5193-4022-a3b1-ade9be1337e8","ExtractStrokes","ExtractStrokes method [Tablet PC]","ExtractStrokes method [Tablet PC]","IInkDisp interface","IInkDisp interface [Tablet PC]","ExtractStrokes method","IInkDisp.ExtractStrokes","IInkDisp::ExtractStrokes","msinkaut/IInkDisp::ExtractStrokes","tablet.inkdisp_extractstrokes"]
old-location: tablet\inkdisp_extractstrokes.htm
tech.root: tablet
ms.assetid: 1cb109e5-5193-4022-a3b1-ade9be1337e8
ms.date: 12/05/2018
ms.keywords: 1cb109e5-5193-4022-a3b1-ade9be1337e8, ExtractStrokes, ExtractStrokes method [Tablet PC], ExtractStrokes method [Tablet PC],IInkDisp interface, IInkDisp interface [Tablet PC],ExtractStrokes method, IInkDisp.ExtractStrokes, IInkDisp::ExtractStrokes, msinkaut/IInkDisp::ExtractStrokes, tablet.inkdisp_extractstrokes
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
 - IInkDisp::ExtractStrokes
 - msinkaut/IInkDisp::ExtractStrokes
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
 - IInkDisp.ExtractStrokes
---

# IInkDisp::ExtractStrokes


## -description

Specifies the strokes to extract from an <a href="/windows/desktop/tablet/inkdisp-class">InkDisp Class</a> and cut or copy into a new <b>InkDisp Class</b>, by using the known collection of strokes to determine which strokes to extract.

## -parameters

### -param Strokes [in, optional]

Optional. Specifies the collection of strokes to extract. The default value is 0, which specifies that all strokes are extracted.

### -param ExtractFlags [in, optional]

Optional. Specifies the <a href="/windows/desktop/api/msinkaut/ne-msinkaut-inkextractflags">InkExtractFlags Enumeration</a> type, which specifies whether the ink is cut or copied into the new Ink object. The default value is IEF_DEFAULT, which cuts the strokes.

### -param ExtractedInk [out, retval]

When this method returns, contains a pointer to a new <a href="/windows/desktop/tablet/inkdisp-class">InkDisp Class</a> object that contains the extracted collection of cut or copied strokes.

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
Success

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
<dt><b>E_INK_MISMATCHED_INK_OBJECT</b></dt>
</dl>
</td>
<td width="60%">
The <a href="/windows/desktop/tablet/inkdisp-class">InkDisp Class</a> object of the <a href="/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes Collection</a> collection must match the known <b>InkDisp Class</b>.


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
Cannot allocate memory that is used to perform the operation.
              

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
The 
              <a href="/windows/desktop/tablet/inkdisp-class">InkDisp Class</a> object class is not registered.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-extractwithrectangle">ExtractWithRectangle Method</a>



<a href="../msinkaut/nn-msinkaut-iinkdisp.md">IInkDisp</a>



<a href="/windows/desktop/tablet/inkdisp-class">InkDisp Class</a>
