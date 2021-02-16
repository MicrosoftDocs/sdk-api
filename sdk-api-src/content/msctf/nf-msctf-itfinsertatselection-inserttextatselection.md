---
UID: NF:msctf.ITfInsertAtSelection.InsertTextAtSelection
title: ITfInsertAtSelection::InsertTextAtSelection (msctf.h)
description: ITfInsertAtSelection::InsertTextAtSelection method
helpviewer_keywords: ["ITfInsertAtSelection interface [Text Services Framework]","InsertTextAtSelection method","ITfInsertAtSelection.InsertTextAtSelection","ITfInsertAtSelection::InsertTextAtSelection","InsertTextAtSelection","InsertTextAtSelection method [Text Services Framework]","InsertTextAtSelection method [Text Services Framework]","ITfInsertAtSelection interface","TF_IAS_NOQUERY","TF_IAS_NO_DEFAULT_COMPOSITION","TF_IAS_QUERYONLY","_tsf_itfinsertatselection_inserttextatselection_ref","msctf/ITfInsertAtSelection::InsertTextAtSelection","tsf.itfinsertatselection_inserttextatselection"]
old-location: tsf\itfinsertatselection_inserttextatselection.htm
tech.root: TSF
ms.assetid: 1373fe9b-6c51-4514-a7da-c1f872d9b1ce
ms.date: 12/05/2018
ms.keywords: ITfInsertAtSelection interface [Text Services Framework],InsertTextAtSelection method, ITfInsertAtSelection.InsertTextAtSelection, ITfInsertAtSelection::InsertTextAtSelection, InsertTextAtSelection, InsertTextAtSelection method [Text Services Framework], InsertTextAtSelection method [Text Services Framework],ITfInsertAtSelection interface, TF_IAS_NOQUERY, TF_IAS_NO_DEFAULT_COMPOSITION, TF_IAS_QUERYONLY, _tsf_itfinsertatselection_inserttextatselection_ref, msctf/ITfInsertAtSelection::InsertTextAtSelection, tsf.itfinsertatselection_inserttextatselection
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
req.dll: Msctf.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - ITfInsertAtSelection::InsertTextAtSelection
 - msctf/ITfInsertAtSelection::InsertTextAtSelection
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
 - ITfInsertAtSelection.InsertTextAtSelection
---

# ITfInsertAtSelection::InsertTextAtSelection


## -description

Inserts text at the selection or insertion point.

## -parameters

### -param ec [in]

Identifies the edit context. This is obtained from <a href="/windows/desktop/api/msctf/nf-msctf-itfdocumentmgr-createcontext">ITfDocumentMgr::CreateContext</a> or <a href="/windows/desktop/api/msctf/nf-msctf-itfeditsession-doeditsession">ITfEditSession::DoEditSession</a>.

### -param dwFlags [in]

Bit field with one of the following values.

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
<i>ppRange</i> is <b>NULL</b>. This flag cannot be combined with the TF_IAS_QUERYONLY flag.

</td>
</tr>
<tr>
<td width="40%"><a id="TF_IAS_QUERYONLY"></a><a id="tf_ias_queryonly"></a><dl>
<dt><b>TF_IAS_QUERYONLY</b></dt>
</dl>
</td>
<td width="60%">
The context is not modified, but <i>ppRange</i> is set as if the insert had occurred. Read-only access is sufficient. If this flag is not set, <i>ec</i> must have read/write access. This flag cannot be combined with the TF_IAS_NOQUERY flag.

</td>
</tr>
<tr>
<td width="40%"><a id="TF_IAS_NO_DEFAULT_COMPOSITION"></a><a id="tf_ias_no_default_composition"></a><dl>
<dt><b>TF_IAS_NO_DEFAULT_COMPOSITION</b></dt>
</dl>
</td>
<td width="60%">
The manager will not create a default composition if a composition is required. The caller must create a composition object that covers the inserted text before releasing the context lock.

</td>
</tr>
</table>

### -param pchText [in]

Specifies the text to insert.

### -param cch [in]

Specifies the character count of the text in <i>pchText</i>.

### -param ppRange [out]

Receives the position of the inserted object.

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
<dt><b>TF_E_NOLOCK</b></dt>
</dl>
</td>
<td width="60%">
The text service does not have a document lock

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TF_E_DISCONNECTED</b></dt>
</dl>
</td>
<td width="60%">
Context object is not on a document stack.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TS_E_NOSELECTION</b></dt>
</dl>
</td>
<td width="60%">
Context has no selection.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TS_E_READONLY</b></dt>
</dl>
</td>
<td width="60%">
Selection is read-only.

</td>
</tr>
</table>

## -remarks

To insert an <a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a> object instead of text, use <a href="/windows/desktop/api/msctf/nf-msctf-itfinsertatselection-insertembeddedatselection">ITfInsertAtSelection::InsertEmbeddedAtSelection</a>.

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfdocumentmgr-createcontext">ITfDocumentMgr::CreateContext
      </a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfeditsession-doeditsession">ITfEditSession::DoEditSession
      </a>



<a href="/windows/desktop/api/msctf/nn-msctf-itfinsertatselection">ITfInsertAtSelection
      </a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfinsertatselection-insertembeddedatselection">ITfInsertAtSelection::InsertEmbeddedAtSelection
      </a>