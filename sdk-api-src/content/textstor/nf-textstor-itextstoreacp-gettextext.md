---
UID: NF:textstor.ITextStoreACP.GetTextExt
title: ITextStoreACP::GetTextExt (textstor.h)
description: The ITextStoreACP::GetTextExt method returns the bounding box, in screen coordinates, of the text at a specified character position. The caller must have a read-only lock on the document before calling this method.
helpviewer_keywords: ["GetTextExt","GetTextExt method [Text Services Framework]","GetTextExt method [Text Services Framework]","ITextStoreACP interface","ITextStoreACP interface [Text Services Framework]","GetTextExt method","ITextStoreACP.GetTextExt","ITextStoreACP::GetTextExt","_tsf_itextstoreacp_gettextext_ref","textstor/ITextStoreACP::GetTextExt","tsf.itextstoreacp_gettextext"]
old-location: tsf\itextstoreacp_gettextext.htm
tech.root: TSF
ms.assetid: d621e96b-d357-4468-8a89-89445fb1ca9e
ms.date: 12/05/2018
ms.keywords: GetTextExt, GetTextExt method [Text Services Framework], GetTextExt method [Text Services Framework],ITextStoreACP interface, ITextStoreACP interface [Text Services Framework],GetTextExt method, ITextStoreACP.GetTextExt, ITextStoreACP::GetTextExt, _tsf_itextstoreacp_gettextext_ref, textstor/ITextStoreACP::GetTextExt, tsf.itextstoreacp_gettextext
req.header: textstor.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - ITextStoreACP::GetTextExt
 - textstor/ITextStoreACP::GetTextExt
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
 - ITextStoreACP.GetTextExt
---

# ITextStoreACP::GetTextExt


## -description

The <b>ITextStoreACP::GetTextExt</b> method returns the bounding box, in screen coordinates, of the text at a specified character position. The caller must have a read-only lock on the document before calling this method.

## -parameters

### -param vcView [in]

Specifies the context view.

### -param acpStart [in]

Specifies the starting character position of the text to get in the document.

### -param acpEnd [in]

Specifies the ending character position of the text to get in the document.

### -param prc [out]

Receives the bounding box in screen coordinates of the text at the specified character positions.

### -param pfClipped [out]

Receives a Boolean value that specifies if the text in the bounding box has been clipped. If this parameter is <b>TRUE</b>, the bounding box contains clipped text and does not include the entire requested text range. The bounding box is clipped because the requested range is not visible.

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
The range specified by the <i>acpStart</i> and <i>acpEnd</i> parameters extends past the beginning or end of the document.

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

<a href="/windows/desktop/api/textstor/nn-textstor-itextstoreacp">ITextStoreACP</a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfcontextowner-gettextext">ITfContextOwner::GetTextExt
      </a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfcontextview-gettextext">ITfContextView::GetTextExt
      </a>