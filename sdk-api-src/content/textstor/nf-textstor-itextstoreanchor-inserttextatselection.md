---
UID: NF:textstor.ITextStoreAnchor.InsertTextAtSelection
title: ITextStoreAnchor::InsertTextAtSelection (textstor.h)
description: ITextStoreAnchor::InsertTextAtSelection method
helpviewer_keywords: ["ITextStoreAnchor interface [Text Services Framework]","InsertTextAtSelection method","ITextStoreAnchor.InsertTextAtSelection","ITextStoreAnchor::InsertTextAtSelection","InsertTextAtSelection","InsertTextAtSelection method [Text Services Framework]","InsertTextAtSelection method [Text Services Framework]","ITextStoreAnchor interface","TF_IAS_NOQUERY","TF_IAS_QUERYONLY","textstor/ITextStoreAnchor::InsertTextAtSelection","tsf.itextstoreanchor_inserttextatselection"]
old-location: tsf\itextstoreanchor_inserttextatselection.htm
tech.root: TSF
ms.assetid: f5cb512a-d9f5-451f-b6cb-2020ba32e855
ms.date: 12/05/2018
ms.keywords: ITextStoreAnchor interface [Text Services Framework],InsertTextAtSelection method, ITextStoreAnchor.InsertTextAtSelection, ITextStoreAnchor::InsertTextAtSelection, InsertTextAtSelection, InsertTextAtSelection method [Text Services Framework], InsertTextAtSelection method [Text Services Framework],ITextStoreAnchor interface, TF_IAS_NOQUERY, TF_IAS_QUERYONLY, textstor/ITextStoreAnchor::InsertTextAtSelection, tsf.itextstoreanchor_inserttextatselection
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
 - ITextStoreAnchor::InsertTextAtSelection
 - textstor/ITextStoreAnchor::InsertTextAtSelection
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
 - ITextStoreAnchor.InsertTextAtSelection
---

# ITextStoreAnchor::InsertTextAtSelection


## -description

Inserts text at the insertion point or selection.

## -parameters

### -param dwFlags [in]

Specifies whether the <i>paStart</i> and <i>paEnd</i> parameters will contain the results of the text insertion.

The <a href="/windows/desktop/TSF/tf-ias--constants">TF_IAS_NOQUERY</a> and TF_IAS_QUERYONLY flags cannot be combined.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TF_IAS_NOQUERY"></a><a id="tf_ias_noquery"></a><dl>
<dt><b>TF_IAS_NOQUERY</b></dt>
</dl>
</td>
<td width="60%">
Text is inserted, and the values of the <i>ppaStart</i> and <i>ppaEnd</i> parameters can be <b>NULL</b>. Use this flag if the results of the text insertion are not required.

</td>
</tr>
<tr>
<td width="40%"><a id="TF_IAS_QUERYONLY"></a><a id="tf_ias_queryonly"></a><dl>
<dt><b>TF_IAS_QUERYONLY</b></dt>
</dl>
</td>
<td width="60%">
Text is not inserted, and the <i>ppaStart</i> and <i>ppaEnd</i> anchors contain the results of the text insertion. The values of these parameters depend on how the application implements text insertion into a document. Use this flag to view the results of the text insertion without actually inserting the text. Zero-length text can be inserted.

</td>
</tr>
</table>

### -param pchText [in]

Pointer to the string to insert in the document. The string can be <b>NULL</b> terminated.

### -param cch [in]

Specifies the text length.

### -param ppaStart [out]

Pointer to the anchor object at the start of the text insertion.

### -param ppaEnd [out]

Pointer to the anchor object at the end of the text insertion. For an insertion point, this parameter value will be the same as the value of the <i>ppaStart</i> parameter.

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
The method could not instantiate one of the anchors <i>paStart</i> or <i>paEnd</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>pchText</i> parameter is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TS_E_NOLOCK</b></dt>
</dl>
</td>
<td width="60%">
The caller does not have a lock on the document.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/TSF/compositions">Compositions</a>



<a href="/windows/desktop/api/textstor/nn-textstor-itextstoreanchor">ITextStoreAnchor</a>



<a href="/windows/desktop/api/textstor/nf-textstor-itextstoreanchorsink-ontextchange">ITextStoreAnchorSink::OnTextChange
      </a>



<a href="/windows/desktop/TSF/tf-ias--constants">TF_IAS_* Constants
      </a>



<a href="/windows/desktop/api/textstor/ns-textstor-ts_textchange">TS_TEXTCHANGE
      </a>