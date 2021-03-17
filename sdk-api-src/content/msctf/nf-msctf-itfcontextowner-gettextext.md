---
UID: NF:msctf.ITfContextOwner.GetTextExt
title: ITfContextOwner::GetTextExt (msctf.h)
description: The ITfContextOwner::GetTextExt method returns the bounding box, in screen coordinates, of the text at a specified character position. The caller must have a read-only lock on the document before calling this method.
helpviewer_keywords: ["GetTextExt","GetTextExt method [Text Services Framework]","GetTextExt method [Text Services Framework]","ITfContextOwner interface","ITfContextOwner interface [Text Services Framework]","GetTextExt method","ITfContextOwner.GetTextExt","ITfContextOwner::GetTextExt","_tsf_itfcontextowner_gettextext_ref","msctf/ITfContextOwner::GetTextExt","tsf.itfcontextowner_gettextext"]
old-location: tsf\itfcontextowner_gettextext.htm
tech.root: TSF
ms.assetid: edde0ba7-1d88-4c32-b794-761b66d73507
ms.date: 12/05/2018
ms.keywords: GetTextExt, GetTextExt method [Text Services Framework], GetTextExt method [Text Services Framework],ITfContextOwner interface, ITfContextOwner interface [Text Services Framework],GetTextExt method, ITfContextOwner.GetTextExt, ITfContextOwner::GetTextExt, _tsf_itfcontextowner_gettextext_ref, msctf/ITfContextOwner::GetTextExt, tsf.itfcontextowner_gettextext
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.dll: Msimtf.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - ITfContextOwner::GetTextExt
 - msctf/ITfContextOwner::GetTextExt
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msimtf.dll
api_name:
 - ITfContextOwner.GetTextExt
---

# ITfContextOwner::GetTextExt


## -description

The <b>ITfContextOwner::GetTextExt</b> method returns the bounding box, in screen coordinates, of the text at a specified character position. The caller must have a read-only lock on the document before calling this method.

## -parameters

### -param acpStart [in]

Specifies the starting character position of the text to get in the document.

### -param acpEnd [in]

Specifies the ending character position of the text to get in the document.

### -param prc [out]

Receives the bounding box, in screen coordinates, of the text at the specified character positions.

### -param pfClipped [out]

Receives the Boolean value that specifies if the text in the bounding box has been clipped. If this parameter is <b>TRUE</b>, the bounding box contains clipped text and does not include the entire requested range of text. The bounding box is clipped because of the requested range is not visible.

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
<dt><b>TS_E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The specified start and end character positions are equal.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TS_E_INVALIDPOS</b></dt>
</dl>
</td>
<td width="60%">
The range specified by the <i>acpStart</i> and <i>acpEnd</i> parameters extends past the end of the document or the top of the document.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TS_E_NOLAYOUT</b></dt>
</dl>
</td>
<td width="60%">
The application has not calculated a text layout.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TS_E_NOLOCK</b></dt>
</dl>
</td>
<td width="60%">
The caller does not have a read-only lock on the document.

</td>
</tr>
</table>

## -remarks

If the document window is minimized, or if the specified text is not currently visible, the method returns S_OK with the <i>prc</i> parameter set to {0,0,0,0}.

## -see-also

<a href="/windows/desktop/api/textstor/nf-textstor-itextstoreacp-gettextext">ITextStoreACP::GetTextExt
      </a>



<a href="/windows/desktop/api/msctf/nn-msctf-itfcontextowner">ITfContextOwner</a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfcontextview-gettextext">ITfContextView::GetTextExt
      </a>