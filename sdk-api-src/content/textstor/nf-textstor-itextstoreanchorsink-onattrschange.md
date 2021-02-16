---
UID: NF:textstor.ITextStoreAnchorSink.OnAttrsChange
title: ITextStoreAnchorSink::OnAttrsChange (textstor.h)
description: The ITextStoreAnchorSink::OnAttrsChange method is called when the value of one or more text attributes changes.
helpviewer_keywords: ["ITextStoreAnchorSink interface [Text Services Framework]","OnAttrsChange method","ITextStoreAnchorSink.OnAttrsChange","ITextStoreAnchorSink::OnAttrsChange","OnAttrsChange","OnAttrsChange method [Text Services Framework]","OnAttrsChange method [Text Services Framework]","ITextStoreAnchorSink interface","_tsf_itextstoreanchorsink_onattrschange_ref","textstor/ITextStoreAnchorSink::OnAttrsChange","tsf.itextstoreanchorsink_onattrschange"]
old-location: tsf\itextstoreanchorsink_onattrschange.htm
tech.root: TSF
ms.assetid: aa7226dd-1d4a-44ed-94b7-b93813bca2f8
ms.date: 12/05/2018
ms.keywords: ITextStoreAnchorSink interface [Text Services Framework],OnAttrsChange method, ITextStoreAnchorSink.OnAttrsChange, ITextStoreAnchorSink::OnAttrsChange, OnAttrsChange, OnAttrsChange method [Text Services Framework], OnAttrsChange method [Text Services Framework],ITextStoreAnchorSink interface, _tsf_itextstoreanchorsink_onattrschange_ref, textstor/ITextStoreAnchorSink::OnAttrsChange, tsf.itextstoreanchorsink_onattrschange
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
 - ITextStoreAnchorSink::OnAttrsChange
 - textstor/ITextStoreAnchorSink::OnAttrsChange
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
 - ITextStoreAnchorSink.OnAttrsChange
---

# ITextStoreAnchorSink::OnAttrsChange


## -description

The <b>ITextStoreAnchorSink::OnAttrsChange</b> method is called when the value of one or more text attributes changes.

## -parameters

### -param paStart [in]

Pointer to the start anchor of the range of text that has the attribute change.

### -param paEnd [in]

Pointer to the end anchor of the range of text that has the attribute change.

### -param cAttrs [in]

Specifies the number of attributes in the <i>paAttrs</i> array.

### -param paAttrs [in]

Pointer to an array of <a href="/windows/desktop/TSF/ts-attrid">TS_ATTRID</a> values that identify the attributes changed.

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
One or more parameters are invalid.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/textstor/nf-textstor-itextstoreanchor-findnextattrtransition">ITextStoreAnchor::FindNextAttrTransition
      </a>



<a href="/windows/desktop/api/textstor/nf-textstor-itextstoreanchor-requestattrsatposition">ITextStoreAnchor::RequestAttrsAtPosition
      </a>



<a href="/windows/desktop/api/textstor/nf-textstor-itextstoreanchor-requestattrstransitioningatposition">ITextStoreAnchor::RequestAttrsTransitioningAtPosition
      </a>



<a href="/windows/desktop/api/textstor/nf-textstor-itextstoreanchor-requestsupportedattrs">ITextStoreAnchor::RequestSupportedAttrs
      </a>



<a href="/windows/desktop/api/textstor/nn-textstor-itextstoreanchorsink">ITextStoreAnchorSink</a>