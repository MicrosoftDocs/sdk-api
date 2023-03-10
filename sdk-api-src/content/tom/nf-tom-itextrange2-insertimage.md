---
UID: NF:tom.ITextRange2.InsertImage
title: ITextRange2::InsertImage (tom.h)
description: Inserts an image into this range.
helpviewer_keywords: ["ITextRange2 interface [Windows Controls]","InsertImage method","ITextRange2.InsertImage","ITextRange2::InsertImage","InsertImage","InsertImage method [Windows Controls]","InsertImage method [Windows Controls]","ITextRange2 interface","TA_BASELINE","TA_BOTTOM","TA_TOP","controls.itextrange2_insertimage","tom/ITextRange2::InsertImage"]
old-location: controls\itextrange2_insertimage.htm
tech.root: Controls
ms.assetid: CBC71EDC-CBE3-4C44-84C8-6AE6DEBC8D0C
ms.date: 12/05/2018
ms.keywords: ITextRange2 interface [Windows Controls],InsertImage method, ITextRange2.InsertImage, ITextRange2::InsertImage, InsertImage, InsertImage method [Windows Controls], InsertImage method [Windows Controls],ITextRange2 interface, TA_BASELINE, TA_BOTTOM, TA_TOP, controls.itextrange2_insertimage, tom/ITextRange2::InsertImage
req.header: tom.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Msftedit.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITextRange2::InsertImage
 - tom/ITextRange2::InsertImage
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msftedit.dll
api_name:
 - ITextRange2.InsertImage
---

# ITextRange2::InsertImage


## -description

Inserts an image into this range.

## -parameters

### -param width [in]

Type: <b>long</b>

The width, in HIMETRIC units (0.01 mm), of the image.

### -param height [in]

Type: <b>long</b>

The height, in HIMETRIC units, of the image.

### -param ascent [in]

Type: <b>long</b>

If <i>Type</i> is TA_BASELINE, this parameter is the distance, in HIMETRIC units, that the top of the image extends above the text baseline. If <i>Type</i> is TA_BASELINE and <i>ascent</i> is zero, the bottom of the image is placed at the text baseline.

### -param Type [in]

Type: <b>long</b>

The vertical alignment of the image. It can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TA_BASELINE"></a><a id="ta_baseline"></a><dl>
<dt><b>TA_BASELINE</b></dt>
</dl>
</td>
<td width="60%">
Align the image relative to the text baseline. 

</td>
</tr>
<tr>
<td width="40%"><a id="TA_BOTTOM"></a><a id="ta_bottom"></a><dl>
<dt><b>TA_BOTTOM</b></dt>
</dl>
</td>
<td width="60%">
Align the bottom of the image at the bottom of the text line. 

</td>
</tr>
<tr>
<td width="40%"><a id="TA_TOP"></a><a id="ta_top"></a><dl>
<dt><b>TA_TOP</b></dt>
</dl>
</td>
<td width="60%">
Align the top of the image at the top of the text line

</td>
</tr>
</table>

### -param bstrAltText [in]

Type: <b><a href="/previous-versions/windows/desktop/automat/bstr">BSTR</a></b>

The alternate text for the image.

### -param pStream [in]

Type: <b><a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a></b>

The stream that contains the image data.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

If the range is nondegenerate, the image replaces the text in the range.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextrange2">ITextRange2</a>