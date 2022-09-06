---
UID: NF:textstor.ITextStoreAnchor.GetAnchorFromPoint
title: ITextStoreAnchor::GetAnchorFromPoint (textstor.h)
description: The ITextStoreAnchor::GetAnchorFromPoint method converts a point in screen coordinates to an anchor positioned at a corresponding location.
helpviewer_keywords: ["GXFPF_NEAREST","GXFPF_ROUND_NEAREST","GetAnchorFromPoint","GetAnchorFromPoint method [Text Services Framework]","GetAnchorFromPoint method [Text Services Framework]","ITextStoreAnchor interface","ITextStoreAnchor interface [Text Services Framework]","GetAnchorFromPoint method","ITextStoreAnchor.GetAnchorFromPoint","ITextStoreAnchor::GetAnchorFromPoint","textstor/ITextStoreAnchor::GetAnchorFromPoint","tsf.itextstoreanchor_getanchorfrompoint"]
old-location: tsf\itextstoreanchor_getanchorfrompoint.htm
tech.root: TSF
ms.assetid: 5567b53e-540e-41ce-b890-f2e4c5b06c57
ms.date: 12/05/2018
ms.keywords: GXFPF_NEAREST, GXFPF_ROUND_NEAREST, GetAnchorFromPoint, GetAnchorFromPoint method [Text Services Framework], GetAnchorFromPoint method [Text Services Framework],ITextStoreAnchor interface, ITextStoreAnchor interface [Text Services Framework],GetAnchorFromPoint method, ITextStoreAnchor.GetAnchorFromPoint, ITextStoreAnchor::GetAnchorFromPoint, textstor/ITextStoreAnchor::GetAnchorFromPoint, tsf.itextstoreanchor_getanchorfrompoint
req.header: textstor.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Textstor.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Msctf.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - ITextStoreAnchor::GetAnchorFromPoint
 - textstor/ITextStoreAnchor::GetAnchorFromPoint
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msctf.dll
api_name:
 - ITextStoreAnchor.GetAnchorFromPoint
---

# ITextStoreAnchor::GetAnchorFromPoint


## -description

The <b>ITextStoreAnchor::GetAnchorFromPoint</b> method converts a point in screen coordinates to an anchor positioned at a corresponding location.

## -parameters

### -param vcView [in]

Specifies the context view.

### -param ptScreen [in]

Pointer to the <b>POINT</b> structure with the screen coordinates of the point.

### -param dwFlags [in]

Specifies the anchor position to return based upon the screen coordinates of the point relative to a character bounding box. By default, the anchor position returned is the character bounding box containing the screen coordinates of the point. If the point is outside a character bounding box, the method returns <b>NULL</b> or <a href="/windows/desktop/TSF/manager-return-values">TF_E_INVALIDPOINT</a>. Other bit flags for this parameter are as follows.

The bit flags can be combined.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="GXFPF_ROUND_NEAREST"></a><a id="gxfpf_round_nearest"></a><dl>
<dt><b>GXFPF_ROUND_NEAREST</b></dt>
</dl>
</td>
<td width="60%">
If the screen coordinates of the point are contained in a character bounding box, an anchor is returned at the bounding edge closest to the screen coordinates of the point.

</td>
</tr>
<tr>
<td width="40%"><a id="GXFPF_NEAREST"></a><a id="gxfpf_nearest"></a><dl>
<dt><b>GXFPF_NEAREST</b></dt>
</dl>
</td>
<td width="60%">
If the screen coordinates of the point are not contained in a character bounding box, an anchor at the closest character position is returned.

</td>
</tr>
</table>

### -param ppaSite [out]

Pointer to an anchor object at a location corresponding to the screen coordinates <i>ptScreen</i>.

## -returns

This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The method failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more input parameters is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The attempt to instantiate an anchor at the specified location failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TS_E_INVALIDPOINT</b></dt>
</dl>
</td>
<td width="60%">
The <i>ptScreen</i> parameter is not within the bounding box of any character.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TS_E_NOLAYOUT</b></dt>
</dl>
</td>
<td width="60%">
The application has not calculated a text layout yet.

</td>
</tr>
</table>

## -remarks

<img alt="Point 1 is in character bounding box and point 2 is outside the character bounding box." border="border" src="./images/ACPFig01.gif"/>
The point 1 screen coordinates cause the offset (character position) of anchor <i>ppaSite</i> to be 0 by default or if the <i>dwFlags</i> parameter is set to <a href="/windows/desktop/TSF/gxfpf--constants">GXFPF_NEAREST</a> because the point 1 screen coordinates are inside the character bounding box of character position 0. If the <i>dwFlags</i> parameter is set to GXFPF_ROUND_NEAREST for point 1, the anchor offset is 1 because the point 1 screen coordinates are closest to range position 1. Range position 1 is the starting range position of character position 1.

For the point 2 screen coordinates, the method returns <b>TF_E_INVALIDPOINT</b> by default or if the <i>dwFlags</i> parameter is set to <b>GXFPF_NEAREST</b> because the point 2 screen coordinates are outside a character bounding box. If the <i>dwFlags</i> parameter is set to <b>GXFPF_ROUND_NEAREST</b>, then the point 2 screen coordinates causes the anchor offset to be 1, because the closest character position to the point 2 screen coordinates is character position 1.

<b>Point 1</b>

<ul>
<li>Default-- <i>anchor offset = 0</i> --The screen coordinates point is inside the character bounding box of Character Position 0.</li>
<li><b>GXFPF_ROUND_NEAREST</b> -- <i>anchor offset = 1</i> --The screen coordinates of the point is closest to Range Position 1 which is the starting range position of Character Position 1.</li>
<li><b>GXFPF_NEAREST</b> -- <i>anchor offset = 0</i> --The default behavior occurs because the point is within the character bounding box of Character Position 0.</li>
</ul>
<b>Point 2</b>

<ul>
<li>Default-- <i>hr = TF_E_INVALIDPOINT</i> --The screen coordinates of the point are outside a character bounding box.</li>
<li>GXFPF_ROUND_NEAREST-- <i>hr = TF_E_INVALIDPOINT</i> --The default behavior occurs because the screen coordinates of the point is outside a character bounding box.</li>
<li>GXFPF_NEAREST-- <i>anchor offset = 1</i> --The closest character position to the screen coordinates of the point is Character Position 1.</li>
</ul>

## -see-also

<a href="/windows/desktop/TSF/gxfpf--constants">GXFPF_* Constants
      </a>



<a href="/windows/desktop/api/textstor/nn-textstor-itextstoreanchor">ITextStoreAnchor</a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfcontextview-getrangefrompoint">ITfContextView::GetRangeFromPoint
      </a>



<a href="/windows/desktop/TSF/manager-return-values">Manager Return Values
      </a>



<a href="/windows/desktop/TSF/tsviewcookie">TsViewCookie
      </a>