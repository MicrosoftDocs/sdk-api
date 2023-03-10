---
UID: NF:textstor.ITextStoreACP2.GetTextExt
title: ITextStoreACP2::GetTextExt (textstor.h)
description: Gets the bounding box, in screen coordinates, of the text at a specified character position. The caller must have a read-only lock on the document before calling this method.
helpviewer_keywords: ["GetTextExt","GetTextExt method [Text Services Framework]","GetTextExt method [Text Services Framework]","ITextStoreACP2 interface","ITextStoreACP2 interface [Text Services Framework]","GetTextExt method","ITextStoreACP2.GetTextExt","ITextStoreACP2::GetTextExt","textstor/ITextStoreACP2::GetTextExt","tsf.itextstoreacp2_gettextext"]
old-location: tsf\itextstoreacp2_gettextext.htm
tech.root: TSF
ms.assetid: 44ede856-f4e7-4d82-8a15-c79a95e4994f
ms.date: 12/05/2018
ms.keywords: GetTextExt, GetTextExt method [Text Services Framework], GetTextExt method [Text Services Framework],ITextStoreACP2 interface, ITextStoreACP2 interface [Text Services Framework],GetTextExt method, ITextStoreACP2.GetTextExt, ITextStoreACP2::GetTextExt, textstor/ITextStoreACP2::GetTextExt, tsf.itextstoreacp2_gettextext
req.header: textstor.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITextStoreACP2::GetTextExt
 - textstor/ITextStoreACP2::GetTextExt
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
 - ITextStoreACP2.GetTextExt
---

# ITextStoreACP2::GetTextExt


## -description

Gets the bounding box, in screen coordinates, of the text at a specified character position. The caller must have a read-only lock on the document before calling this method.

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

If the document window is minimized, or if the specified text is not currently visible, the method returns <b>S_OK</b> with the <i>prc</i> parameter set to {0,0,0,0}.

## -see-also

<a href="/windows/desktop/api/textstor/nn-textstor-itextstoreacp2">ITextStoreACP2</a>