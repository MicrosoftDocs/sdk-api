---
UID: NF:textstor.ITextStoreACP.InsertTextAtSelection
title: ITextStoreACP::InsertTextAtSelection (textstor.h)
description: The ITextStoreACP::InsertTextAtSelection method inserts text at the insertion point or selection. A caller must have a read/write lock on the document before inserting text.
helpviewer_keywords: ["0","ITextStoreACP interface [Text Services Framework]","InsertTextAtSelection method","ITextStoreACP.InsertTextAtSelection","ITextStoreACP::InsertTextAtSelection","InsertTextAtSelection","InsertTextAtSelection method [Text Services Framework]","InsertTextAtSelection method [Text Services Framework]","ITextStoreACP interface","TF_IAS_NOQUERY","TF_IAS_QUERYONLY","_tsf_itextstoreacp_inserttextatselection_ref","acpNewEnd","acpOldEnd","acpStart","textstor/ITextStoreACP::InsertTextAtSelection","tsf.itextstoreacp_inserttextatselection"]
old-location: tsf\itextstoreacp_inserttextatselection.htm
tech.root: TSF
ms.assetid: b57ad8da-6f79-4d27-96e0-608cbcaae826
ms.date: 12/05/2018
ms.keywords: 0, ITextStoreACP interface [Text Services Framework],InsertTextAtSelection method, ITextStoreACP.InsertTextAtSelection, ITextStoreACP::InsertTextAtSelection, InsertTextAtSelection, InsertTextAtSelection method [Text Services Framework], InsertTextAtSelection method [Text Services Framework],ITextStoreACP interface, TF_IAS_NOQUERY, TF_IAS_QUERYONLY, _tsf_itextstoreacp_inserttextatselection_ref, acpNewEnd, acpOldEnd, acpStart, textstor/ITextStoreACP::InsertTextAtSelection, tsf.itextstoreacp_inserttextatselection
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
 - ITextStoreACP::InsertTextAtSelection
 - textstor/ITextStoreACP::InsertTextAtSelection
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
 - ITextStoreACP.InsertTextAtSelection
---

# ITextStoreACP::InsertTextAtSelection


## -description

The <b>ITextStoreACP::InsertTextAtSelection</b> method inserts text at the insertion point or selection. A caller must have a read/write lock on the document before inserting text.

## -parameters

### -param dwFlags [in]

Specifies whether the <i>pacpStart</i> and <i>pacpEnd</i> parameters and the <a href="/windows/desktop/api/textstor/ns-textstor-ts_textchange">TS_TEXTCHANGE</a> structure contain the results of the text insertion.

The <a href="/windows/desktop/TSF/tf-ias--constants">TF_IAS_NOQUERY</a> and TF_IAS_QUERYONLY flags cannot be combined.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="0"></a><dl>
<dt><b>0</b></dt>
</dl>
</td>
<td width="60%">
Text insertion will occur, and the <i>pacpStart</i> and <i>pacpEnd</i> parameters will contain the results of the text insertion. The <b>TS_TEXTCHANGE</b> structure must be filled with this flag.

</td>
</tr>
<tr>
<td width="40%"><a id="TF_IAS_NOQUERY"></a><a id="tf_ias_noquery"></a><dl>
<dt><b>TF_IAS_NOQUERY</b></dt>
</dl>
</td>
<td width="60%">
Text is inserted, the values of the <i>pacpStart</i> and <i>pacpEnd</i> parameters can be <b>NULL</b>, and the <b>TS_TEXTCHANGE</b> structure must be filled. Use this flag to view the results of the text insertion.

</td>
</tr>
<tr>
<td width="40%"><a id="TF_IAS_QUERYONLY"></a><a id="tf_ias_queryonly"></a><dl>
<dt><b>TF_IAS_QUERYONLY</b></dt>
</dl>
</td>
<td width="60%">
Text is not inserted, and the values for the <i>pacpStart</i> and <i>pacpEnd</i> parameters contain the results of the text insertion. The values of these parameters depend on how the application implements text insertion into a document. For more information, see the Remarks section. Use this flag to view the results of the text insertion without actually inserting the text. It is not required that you fill the <b>TS_TEXTCHANGE</b> structure if you use this flag.

</td>
</tr>
</table>

### -param pchText [in]

Pointer to the string to insert in the document. The string can be <b>NULL</b> terminated.

### -param cch [in]

Specifies the text length.

### -param pacpStart [out]

Pointer to the starting application character position where the text insertion occurs.

### -param pacpEnd [out]

Pointer to the ending application character position where the text insertion occurs. This parameter value is the same as the value of the <i>pacpStart</i> parameter for an insertion point.

### -param pChange [out]

Pointer to a <b>TS_TEXTCHANGE</b> structure with the following members.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="acpStart"></a><a id="acpstart"></a><a id="ACPSTART"></a><dl>
<dt><b>acpStart</b></dt>
</dl>
</td>
<td width="60%">
The starting application character position before the text is inserted into the document.

</td>
</tr>
<tr>
<td width="40%"><a id="acpOldEnd"></a><a id="acpoldend"></a><a id="ACPOLDEND"></a><dl>
<dt><b>acpOldEnd</b></dt>
</dl>
</td>
<td width="60%">
The ending application character position before the text is inserted into the document. This value is the same as <b>acpStart</b> for an insertion point. If this value is different from <b>acpStart</b>, then text was selected prior to the text insertion.

</td>
</tr>
<tr>
<td width="40%"><a id="acpNewEnd"></a><a id="acpnewend"></a><a id="ACPNEWEND"></a><dl>
<dt><b>acpNewEnd</b></dt>
</dl>
</td>
<td width="60%">
The end position after the text insertion occurred.

</td>
</tr>
</table>

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
<dt><b>TS_E_NOLOCK</b></dt>
</dl>
</td>
<td width="60%">
The caller does not have a lock on the document.

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
</table>

## -remarks

The values of the <i>pacpStart</i> and the <i>pacpEnd</i> parameters depend upon how the client application inserts text into a document. For example, if the application sets the cursor at the start of the inserted text after text insertion, then the value for the <i>pacpStart</i> and <i>pacpEnd</i> parameters is the same as the <b>acpStart</b> member of the <b>TS_TEXTCHANGE</b> structure.

Applications should not call the <a href="/windows/desktop/api/textstor/nf-textstor-itextstoreacpsink-ontextchange">ITextStoreACPSink::OnTextChange</a> method in response to this method.

## -see-also

<a href="/windows/desktop/TSF/compositions">Compositions</a>



<a href="/windows/desktop/api/textstor/nn-textstor-itextstoreacp">ITextStoreACP</a>



<a href="/windows/desktop/api/textstor/nf-textstor-itextstoreacpsink-ontextchange">ITextStoreACPSink::OnTextChange
      </a>



<a href="/windows/desktop/TSF/tf-ias--constants">TF_IAS_* Constants
      </a>



<a href="/windows/desktop/api/textstor/ns-textstor-ts_textchange">TS_TEXTCHANGE
      </a>