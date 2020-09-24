---
UID: NF:textstor.ITextStoreAnchor.RequestAttrsAtPosition
title: ITextStoreAnchor::RequestAttrsAtPosition (textstor.h)
description: ITextStoreAnchor::RequestAttrsAtPosition method
helpviewer_keywords: ["ITextStoreAnchor interface [Text Services Framework]","RequestAttrsAtPosition method","ITextStoreAnchor.RequestAttrsAtPosition","ITextStoreAnchor::RequestAttrsAtPosition","RequestAttrsAtPosition","RequestAttrsAtPosition method [Text Services Framework]","RequestAttrsAtPosition method [Text Services Framework]","ITextStoreAnchor interface","textstor/ITextStoreAnchor::RequestAttrsAtPosition","tsf.itextstoreanchor_requestattrsatposition"]
old-location: tsf\itextstoreanchor_requestattrsatposition.htm
tech.root: TSF
ms.assetid: d0f20507-005b-409d-90d5-5817b7d95f19
ms.date: 12/05/2018
ms.keywords: ITextStoreAnchor interface [Text Services Framework],RequestAttrsAtPosition method, ITextStoreAnchor.RequestAttrsAtPosition, ITextStoreAnchor::RequestAttrsAtPosition, RequestAttrsAtPosition, RequestAttrsAtPosition method [Text Services Framework], RequestAttrsAtPosition method [Text Services Framework],ITextStoreAnchor interface, textstor/ITextStoreAnchor::RequestAttrsAtPosition, tsf.itextstoreanchor_requestattrsatposition
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
 - ITextStoreAnchor::RequestAttrsAtPosition
 - textstor/ITextStoreAnchor::RequestAttrsAtPosition
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
 - ITextStoreAnchor.RequestAttrsAtPosition
---

# ITextStoreAnchor::RequestAttrsAtPosition


## -description

Obtains a list of attributes that begin or end at the specified anchor location.

## -parameters

### -param paPos [in]

Pointer to the anchor.

### -param cFilterAttrs [in]

Specifies the number of attributes to obtain.

### -param paFilterAttrs [in]

Pointer to the <a href="/windows/desktop/TSF/ts-attrid">TS_ATTRID</a> data type that specifies the attribute to verify.

### -param dwFlags [in]

Must be zero.

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
The <i>paPos</i> anchor is invalid.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/textstor/nn-textstor-itextstoreanchor">ITextStoreAnchor</a>



<a href="/windows/desktop/api/textstor/nf-textstor-itextstoreanchor-retrieverequestedattrs">ITextStoreAnchor::RetrieveRequestedAttrs
      </a>



<a href="/windows/desktop/TSF/ts-attrid">TS_ATTRID
      </a>