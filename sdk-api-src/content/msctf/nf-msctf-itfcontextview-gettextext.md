---
UID: NF:msctf.ITfContextView.GetTextExt
title: ITfContextView::GetTextExt (msctf.h)
description: The ITfContextView::GetTextExt method returns the bounding box, in screen coordinates, of a range of text.
helpviewer_keywords: ["GetTextExt","GetTextExt method [Text Services Framework]","GetTextExt method [Text Services Framework]","ITfContextView interface","ITfContextView interface [Text Services Framework]","GetTextExt method","ITfContextView.GetTextExt","ITfContextView::GetTextExt","_tsf_itfcontextview_gettextext_ref","msctf/ITfContextView::GetTextExt","tsf.itfcontextview_gettextext"]
old-location: tsf\itfcontextview_gettextext.htm
tech.root: TSF
ms.assetid: a4ef9180-5568-4e5b-8c37-f750263060d2
ms.date: 12/05/2018
ms.keywords: GetTextExt, GetTextExt method [Text Services Framework], GetTextExt method [Text Services Framework],ITfContextView interface, ITfContextView interface [Text Services Framework],GetTextExt method, ITfContextView.GetTextExt, ITfContextView::GetTextExt, _tsf_itfcontextview_gettextext_ref, msctf/ITfContextView::GetTextExt, tsf.itfcontextview_gettextext
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
 - ITfContextView::GetTextExt
 - msctf/ITfContextView::GetTextExt
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
 - ITfContextView.GetTextExt
---

# ITfContextView::GetTextExt


## -description

The <b>ITfContextView::GetTextExt</b> method returns the bounding box, in screen coordinates, of a range of text.

## -parameters

### -param ec [in]

Specifies an edit cookie with read-only access.

### -param pRange [in]

Specifies the range to query

### -param prc [out]

Receives the bounding box, in screen coordinates, of the range.

### -param pfClipped [out]

Receives the Boolean value that specifies if the text in the bounding box has been clipped. If this parameter is <b>TRUE</b>, the bounding box contains clipped text and does not include the entire requested range. The bounding box is clipped because of the requested range is not visible.

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
<dt><b>TS_E_NOLAYOUT</b></dt>
</dl>
</td>
<td width="60%">
The text is not rendered or the context has not calculated the text layout.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TF_E_NOLOCK</b></dt>
</dl>
</td>
<td width="60%">
The edit cookie parameter is invalid.

</td>
</tr>
</table>

## -remarks

If the document window is minimized, or if the specified text is not currently visible, the method returns S_OK with the <i>prc</i> parameter set to {0,0,0,0}.

## -see-also

<a href="/windows/desktop/api/msctf/nf-msctf-itfcontextowner-gettextext">ITfContextOwner::GetTextExt
      </a>



<a href="/windows/desktop/api/msctf/nn-msctf-itfcontextview">ITfContextView</a>