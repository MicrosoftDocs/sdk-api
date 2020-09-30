---
UID: NF:msctf.ITfInsertAtSelection.InsertEmbeddedAtSelection
title: ITfInsertAtSelection::InsertEmbeddedAtSelection (msctf.h)
description: The ITfInsertAtSelection::InsertEmbeddedAtSelection method inserts an IDataObject object at the selection or insertion point.
helpviewer_keywords: ["ITfInsertAtSelection interface [Text Services Framework]","InsertEmbeddedAtSelection method","ITfInsertAtSelection.InsertEmbeddedAtSelection","ITfInsertAtSelection::InsertEmbeddedAtSelection","InsertEmbeddedAtSelection","InsertEmbeddedAtSelection method [Text Services Framework]","InsertEmbeddedAtSelection method [Text Services Framework]","ITfInsertAtSelection interface","_tsf_itfinsertatselection_insertembeddedatselection_ref","msctf/ITfInsertAtSelection::InsertEmbeddedAtSelection","tsf.itfinsertatselection_insertembeddedatselection"]
old-location: tsf\itfinsertatselection_insertembeddedatselection.htm
tech.root: TSF
ms.assetid: 13fa9955-0087-4dd9-8a1d-814ab801e956
ms.date: 12/05/2018
ms.keywords: ITfInsertAtSelection interface [Text Services Framework],InsertEmbeddedAtSelection method, ITfInsertAtSelection.InsertEmbeddedAtSelection, ITfInsertAtSelection::InsertEmbeddedAtSelection, InsertEmbeddedAtSelection, InsertEmbeddedAtSelection method [Text Services Framework], InsertEmbeddedAtSelection method [Text Services Framework],ITfInsertAtSelection interface, _tsf_itfinsertatselection_insertembeddedatselection_ref, msctf/ITfInsertAtSelection::InsertEmbeddedAtSelection, tsf.itfinsertatselection_insertembeddedatselection
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
 - ITfInsertAtSelection::InsertEmbeddedAtSelection
 - msctf/ITfInsertAtSelection::InsertEmbeddedAtSelection
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
 - ITfInsertAtSelection.InsertEmbeddedAtSelection
---

# ITfInsertAtSelection::InsertEmbeddedAtSelection


## -description

The <b>ITfInsertAtSelection::InsertEmbeddedAtSelection</b> method inserts an <a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a> object at the selection or insertion point.

## -parameters

### -param ec [in]

Identifies the edit context. This is obtained from <a href="/windows/desktop/api/msctf/nf-msctf-itfdocumentmgr-createcontext">ITfDocumentMgr::CreateContext</a> or <a href="/windows/desktop/api/msctf/nf-msctf-itfeditsession-doeditsession">ITfEditSession::DoEditSession</a>.

### -param dwFlags [in]

Bit field with one of the following values:

TF_IAS_NOQUERY

The <i>ppRange</i> parameter is <b>NULL</b> on exit.

TF_IAS_QUERYONLY

Context is not modified but the <i>ppRange</i> parameter is set as if the insert occurred. Read-only access is sufficient. If this flag is not set, the <i>ec</i> parameter must have read/write access.

TF_IAS_NO_DEFAULT_COMPOSITION

The TSF manager does not create a default composition if a composition is required. The caller must create a composition object that covers the inserted text before releasing the context lock.

### -param pDataObject [in]

Pointer to object to insert.

### -param ppRange [out]

Position of the inserted object. Optional.

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
The <i>ec</i> parameter is an invalid edit cookie.

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
<tr>
<td width="40%">
<dl>
<dt><b>TF_E_FORMAT</b></dt>
</dl>
</td>
<td width="60%">
Context owner cannot handle objects of the type provided by the <i>pDataObject</i> parameter.

</td>
</tr>
</table>

## -remarks

Callers can use the <a href="/windows/desktop/api/msctf/nf-msctf-itfqueryembedded-queryinsertembedded">ITfQueryEmbedded::QueryInsertEmbedded</a> method to determine if a particular object type is likely to be accepted by this method.

To insert text instead of an <b>IDataObject</b> object, use the <a href="/windows/desktop/api/msctf/nf-msctf-itfinsertatselection-inserttextatselection">ITfInsertAtSelection::InsertTextAtSelection</a> method.

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfdocumentmgr-createcontext">ITfDocumentMgr::CreateContext
      </a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfeditsession-doeditsession">ITfEditSession::DoEditSession
      </a>



<a href="/windows/desktop/api/msctf/nn-msctf-itfinsertatselection">ITfInsertAtSelection
      </a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfinsertatselection-inserttextatselection">ITfInsertAtSelection::InsertTextAtSelection
      </a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfqueryembedded-queryinsertembedded">ITfQueryEmbedded::QueryInsertEmbedded
      </a>