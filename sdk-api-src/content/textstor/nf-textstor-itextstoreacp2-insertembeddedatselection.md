---
UID: NF:textstor.ITextStoreACP2.InsertEmbeddedAtSelection
title: ITextStoreACP2::InsertEmbeddedAtSelection (textstor.h)
description: Inserts an IDataObject at the insertion point or selection. The client that calls this method must have a read/write lock before inserting an IDataObject object into the document.
helpviewer_keywords: ["0","ITextStoreACP2 interface [Text Services Framework]","InsertEmbeddedAtSelection method","ITextStoreACP2.InsertEmbeddedAtSelection","ITextStoreACP2::InsertEmbeddedAtSelection","InsertEmbeddedAtSelection","InsertEmbeddedAtSelection method [Text Services Framework]","InsertEmbeddedAtSelection method [Text Services Framework]","ITextStoreACP2 interface","TF_IAS_NOQUERY","TF_IAS_QUERYONLY","acpNewEnd","acpOldEnd","acpStart","textstor/ITextStoreACP2::InsertEmbeddedAtSelection","tsf.itextstoreacp2_insertembeddedatselection"]
old-location: tsf\itextstoreacp2_insertembeddedatselection.htm
tech.root: TSF
ms.assetid: 677114a5-8c87-4632-b308-2bb6dedf78c8
ms.date: 12/05/2018
ms.keywords: 0, ITextStoreACP2 interface [Text Services Framework],InsertEmbeddedAtSelection method, ITextStoreACP2.InsertEmbeddedAtSelection, ITextStoreACP2::InsertEmbeddedAtSelection, InsertEmbeddedAtSelection, InsertEmbeddedAtSelection method [Text Services Framework], InsertEmbeddedAtSelection method [Text Services Framework],ITextStoreACP2 interface, TF_IAS_NOQUERY, TF_IAS_QUERYONLY, acpNewEnd, acpOldEnd, acpStart, textstor/ITextStoreACP2::InsertEmbeddedAtSelection, tsf.itextstoreacp2_insertembeddedatselection
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
 - ITextStoreACP2::InsertEmbeddedAtSelection
 - textstor/ITextStoreACP2::InsertEmbeddedAtSelection
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
 - ITextStoreACP2.InsertEmbeddedAtSelection
---

# ITextStoreACP2::InsertEmbeddedAtSelection


## -description

Inserts an <a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a> at the insertion point or selection. The client that calls this method must have a read/write lock before inserting an <a href="/windows/desktop/api/textstor/nf-textstor-itextstoreacp-insertembeddedatselection">IDataObject</a> object into the document.

## -parameters

### -param dwFlags [in]

Specifies whether the <i>pacpStart</i> and <i>pacpEnd</i> parameters and the <a href="/windows/desktop/api/textstor/ns-textstor-ts_textchange">TS_TEXTCHANGE</a> structure will contain the results of the object insertion.

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
Text insertion will occur, and the <i>pacpStart</i> and <i>pacpEnd</i> parameters will contain the results of the text insertion. The <a href="/windows/desktop/api/textstor/ns-textstor-ts_textchange">TS_TEXTCHANGE</a> structure must be filled with this flag.

</td>
</tr>
<tr>
<td width="40%"><a id="TF_IAS_NOQUERY"></a><a id="tf_ias_noquery"></a><dl>
<dt><b>TF_IAS_NOQUERY</b></dt>
</dl>
</td>
<td width="60%">
Text is inserted, the values of the <i>pacpStart</i> and <i>pacpEnd</i> parameters can be <b>NULL</b>, and the <a href="/windows/desktop/api/textstor/ns-textstor-ts_textchange">TS_TEXTCHANGE</a> structure must be filled. Use this flag if the results of the text insertion are not required.

</td>
</tr>
<tr>
<td width="40%"><a id="TF_IAS_QUERYONLY"></a><a id="tf_ias_queryonly"></a><dl>
<dt><b>TF_IAS_QUERYONLY</b></dt>
</dl>
</td>
<td width="60%">
Text is not inserted, and the values for the <i>pacpStart</i> and <i>pacpEnd</i> parameter contain the results of the text insertion. The values of these parameters depend on how the application implements text insertion into a document. For more information, see the Remarks section.

Use this flag to view the results of the text insertion without actually inserting the text, for example, to predict the results of collapsing or otherwise adjusting a selection. It is not required that you fill the <a href="/windows/desktop/api/textstor/ns-textstor-ts_textchange">TS_TEXTCHANGE</a> structure with this flag.

</td>
</tr>
</table>

### -param pDataObject [in]

Pointer to the <a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a> object to be inserted.

### -param pacpStart [out]

Pointer to the starting application character position where the object insertion will occur.

### -param pacpEnd [out]

Pointer to the ending application character position where the object insertion will occur. This parameter value will be the same as the value of the <i>pacpStart</i> parameter for an insertion point.

### -param pChange [out]

Pointer to a <a href="/windows/desktop/api/textstor/ns-textstor-ts_textchange">TS_TEXTCHANGE</a> structure with the following members.

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
The starting application character position before the object is inserted into the document.

</td>
</tr>
<tr>
<td width="40%"><a id="acpOldEnd"></a><a id="acpoldend"></a><a id="ACPOLDEND"></a><dl>
<dt><b>acpOldEnd</b></dt>
</dl>
</td>
<td width="60%">
The ending application character position before the object is inserted into the document. This value is the same as <b>acpStart</b> for an insertion point. If this value is different from <b>acpStart</b>, then text was selected prior to the object insertion.

</td>
</tr>
<tr>
<td width="40%"><a id="acpNewEnd"></a><a id="acpnewend"></a><a id="ACPNEWEND"></a><dl>
<dt><b>acpNewEnd</b></dt>
</dl>
</td>
<td width="60%">
The ending application character position after the object insertion took place.

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

## -remarks

The values of the <i>pacpStart</i> and <i>pacpEnd</i> parameters depend upon how the client application inserts an object into a document. For example, if the application sets the cursor at the start of the object after object insertion, then the value of the <i>pacpStart</i> and <i>pacpEnd</i> parameters is the same as the <b>acpStart</b> member of the <a href="/windows/desktop/api/textstor/ns-textstor-ts_textchange">TS_TEXTCHANGE</a> structure.

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a>



<a href="/windows/desktop/api/textstor/nn-textstor-itextstoreacp2">ITextStoreACP2</a>



<a href="/windows/desktop/TSF/tf-ias--constants">TF_IAS_* Constants
      </a>



<a href="/windows/desktop/api/textstor/ns-textstor-ts_textchange">TS_TEXTCHANGE</a>