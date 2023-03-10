---
UID: NF:msctf.ITfContextView.GetRangeFromPoint
title: ITfContextView::GetRangeFromPoint (msctf.h)
description: The ITfContextView::GetRangeFromPoint method converts a point, in screen coordinates, to an empty range of text positioned at a corresponding location.
helpviewer_keywords: ["GXFPF_NEAREST","GXFPF_ROUND_NEAREST","GetRangeFromPoint","GetRangeFromPoint method [Text Services Framework]","GetRangeFromPoint method [Text Services Framework]","ITfContextView interface","ITfContextView interface [Text Services Framework]","GetRangeFromPoint method","ITfContextView.GetRangeFromPoint","ITfContextView::GetRangeFromPoint","_tsf_itfcontextview_getrangefrompoint_ref","msctf/ITfContextView::GetRangeFromPoint","tsf.itfcontextview_getrangefrompoint"]
old-location: tsf\itfcontextview_getrangefrompoint.htm
tech.root: TSF
ms.assetid: 543761fe-420e-4821-a69f-abc6c853677e
ms.date: 12/05/2018
ms.keywords: GXFPF_NEAREST, GXFPF_ROUND_NEAREST, GetRangeFromPoint, GetRangeFromPoint method [Text Services Framework], GetRangeFromPoint method [Text Services Framework],ITfContextView interface, ITfContextView interface [Text Services Framework],GetRangeFromPoint method, ITfContextView.GetRangeFromPoint, ITfContextView::GetRangeFromPoint, _tsf_itfcontextview_getrangefrompoint_ref, msctf/ITfContextView::GetRangeFromPoint, tsf.itfcontextview_getrangefrompoint
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
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
 - ITfContextView::GetRangeFromPoint
 - msctf/ITfContextView::GetRangeFromPoint
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
 - ITfContextView.GetRangeFromPoint
---

# ITfContextView::GetRangeFromPoint


## -description

The <b>ITfContextView::GetRangeFromPoint</b> method converts a point, in screen coordinates, to an empty range of text positioned at a corresponding location.

## -parameters

### -param ec [in]

Specifies the edit cookie with read-only access.

### -param ppt [in]

Specifies the point in screen coordinates.

### -param dwFlags [in]

Specifies the range position to return based upon the screen coordinates of the point to a character bounding box. By default, the range position returned is the character bounding box containing the screen coordinates of the point. If the point is outside a character bounding box, the method returns <b>NULL</b> or <a href="/windows/desktop/TSF/manager-return-values">TF_E_INVALIDPOINT</a>. Other bit flags for this parameter are as follows.

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
If the screen coordinates of the point are contained in a character bounding box, the range position returned is the bounding edge closest to the screen coordinates of the point.

</td>
</tr>
<tr>
<td width="40%"><a id="GXFPF_NEAREST"></a><a id="gxfpf_nearest"></a><dl>
<dt><b>GXFPF_NEAREST</b></dt>
</dl>
</td>
<td width="60%">
If the screen coordinates of the point are not contained in a character bounding box, the closest range position is returned.

</td>
</tr>
</table>

### -param ppRange [out]

Receives a pointer to the ITfRange interface.

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
<dt><b>TF_E_INVALIDPOINT</b></dt>
</dl>
</td>
<td width="60%">
The <i>pptScreen</i> parameter does not cover any document text.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TF_E_NOLAYOUT</b></dt>
</dl>
</td>
<td width="60%">
The application has not calculated a text layout.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TF_E_NOLOCK</b></dt>
</dl>
</td>
<td width="60%">
The specified edit cookie is invalid.

</td>
</tr>
</table>

## -remarks

<img alt="Point 1 is in character bounding box and point 2 is outside the character bounding box." border="border" src="./images/RngFig01.gif"/>
By default, the method will return a range positioned at 0 for point 1 and TF_E_INVALIDPOINT for point 2. If the <i>dwFlags</i> parameter is set to <a href="/windows/desktop/TSF/gxfpf--constants">GXFPF_ROUND_NEAREST</a>, the method returns range position 1 for point 1. If the <i>dwFlags</i> parameter is set to GXFPF_NEAREST then the method returns range position 2 for point 2.

## -see-also

<a href="/windows/desktop/TSF/gxfpf--constants">GXFPF_NEAREST
      </a>



GXFPF_ROUND_NEAREST



<a href="/windows/desktop/api/msctf/nn-msctf-itfcontextview">ITfContextView</a>



<a href="/windows/desktop/TSF/manager-return-values">TF_E_INVALIDPOINT</a>