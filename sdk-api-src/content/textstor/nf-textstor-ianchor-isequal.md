---
UID: NF:textstor.IAnchor.IsEqual
title: IAnchor::IsEqual (textstor.h)
description: The IAnchor::IsEqual method evaluates two anchors within a text stream and returns a Boolean value that specifies the equality or inequality of the anchor positions.
helpviewer_keywords: ["IAnchor interface [Text Services Framework]","IsEqual method","IAnchor.IsEqual","IAnchor::IsEqual","IsEqual","IsEqual method [Text Services Framework]","IsEqual method [Text Services Framework]","IAnchor interface","textstor/IAnchor::IsEqual","tsf.ianchor_isequal"]
old-location: tsf\ianchor_isequal.htm
tech.root: TSF
ms.assetid: a2dedce7-f64d-406a-bebc-9a4b51a1ae38
ms.date: 12/05/2018
ms.keywords: IAnchor interface [Text Services Framework],IsEqual method, IAnchor.IsEqual, IAnchor::IsEqual, IsEqual, IsEqual method [Text Services Framework], IsEqual method [Text Services Framework],IAnchor interface, textstor/IAnchor::IsEqual, tsf.ianchor_isequal
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
 - IAnchor::IsEqual
 - textstor/IAnchor::IsEqual
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msctf.dll
api_name:
 - IAnchor.IsEqual
---

# IAnchor::IsEqual


## -description

The <b>IAnchor::IsEqual</b> method evaluates two anchors within a text stream and returns a Boolean value that specifies the equality or inequality of the anchor positions.

## -parameters

### -param paWith [in]

Specifies an anchor to compare to the primary anchor. Used to determine the equality of the two anchor positions.

### -param pfEqual [out]

A Boolean value that specifies whether the two anchors are positioned at the same location. If set to <b>TRUE</b>, the two anchors occupy the same location. If set to <b>FALSE</b>, the two anchors do not occupy the same location.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>pfEqual</i> is invalid.

</td>
</tr>
</table>

## -remarks

Anchors are always positioned between characters or regions. When two anchors are between the same characters, being at the same offset within the text stream, and within the same region, <b>IAnchor::IsEqual</b> returns <b>TRUE</b>. Otherwise it returns <b>FALSE</b>.


<a href="/windows/desktop/api/textstor/nf-textstor-ianchor-compare">IAnchor::Compare
        </a> incorporates the same functionality as <b>IAnchor::IsEqual</b>. However, because <b>IAnchor::IsEqual</b> is more specific, it can have a more efficient implementation on the server.

## -see-also

<a href="/windows/desktop/TSF/ranges">Anchors</a>



<a href="/windows/desktop/api/textstor/nn-textstor-ianchor">IAnchor</a>



<a href="/windows/desktop/api/textstor/nf-textstor-ianchor-compare">IAnchor::Compare
      </a>