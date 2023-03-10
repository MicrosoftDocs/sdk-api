---
UID: NF:msctf.ITfRange.InsertEmbedded
title: ITfRange::InsertEmbedded (msctf.h)
description: The ITfRange::InsertEmbedded method inserts an object at the location of the start anchor of the range of text.
helpviewer_keywords: ["ITfRange interface [Text Services Framework]","InsertEmbedded method","ITfRange.InsertEmbedded","ITfRange::InsertEmbedded","InsertEmbedded","InsertEmbedded method [Text Services Framework]","InsertEmbedded method [Text Services Framework]","ITfRange interface","_tsf_itfrange_insertembedded_ref","msctf/ITfRange::InsertEmbedded","tsf.itfrange_insertembedded"]
old-location: tsf\itfrange_insertembedded.htm
tech.root: TSF
ms.assetid: 95b8622d-c934-4293-abb4-9eface451be5
ms.date: 12/05/2018
ms.keywords: ITfRange interface [Text Services Framework],InsertEmbedded method, ITfRange.InsertEmbedded, ITfRange::InsertEmbedded, InsertEmbedded, InsertEmbedded method [Text Services Framework], InsertEmbedded method [Text Services Framework],ITfRange interface, _tsf_itfrange_insertembedded_ref, msctf/ITfRange::InsertEmbedded, tsf.itfrange_insertembedded
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
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
 - ITfRange::InsertEmbedded
 - msctf/ITfRange::InsertEmbedded
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
 - ITfRange.InsertEmbedded
---

# ITfRange::InsertEmbedded


## -description

The <b>ITfRange::InsertEmbedded</b> method inserts an object at the location of the start anchor of the range of text.

## -parameters

### -param ec [in]

Edit cookie obtained from <a href="/windows/desktop/api/msctf/nf-msctf-itfdocumentmgr-createcontext">ITfDocumentMgr::CreateContext</a> or <a href="/windows/desktop/api/msctf/nf-msctf-itfeditsession-doeditsession">ITfEditSession::DoEditSession</a>.

### -param dwFlags [in]

Bit fields that specify how insertion should occur. If <a href="/windows/desktop/TSF/miscellaneous-framework-constants">TF_IE_CORRECTION</a> is set, the operation is a correction, so that other text services can preserve data associated with the original text.

### -param pDataObject [in]

Pointer to the data transfer object to be inserted.

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
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The implementing application does not expose embedded objects in its stream.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TF_E_COMPOSITION_REJECTED</b></dt>
</dl>
</td>
<td width="60%">
The context owner rejected a default composition.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TF_E_FORMAT</b></dt>
</dl>
</td>
<td width="60%">
The context owner cannot handle the specified object type.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TF_E_NOLOCK</b></dt>
</dl>
</td>
<td width="60%">
The value of the <i>ec</i> parameter is an invalid cookie, or the caller does not have a read-only lock.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TF_E_RANGE_NOT_COVERED</b></dt>
</dl>
</td>
<td width="60%">
The caller already has an active composition, but the range is positioned over text not covered by the composition.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TF_E_READONLY</b></dt>
</dl>
</td>
<td width="60%">
The document or the location of the range cannot be modified.

</td>
</tr>
</table>

## -remarks

Use this method to insert objects into the text stream, because the <a href="/windows/desktop/TSF/miscellaneous-framework-constants">TF_CHAR_EMBEDDED</a> object placeholder character cannot be passed into <a href="/windows/desktop/api/msctf/nf-msctf-itfrange-settext">ITfRange::SetText</a>. This method is modeled after the OLE clipboard API, with applications using <i>pDataObject</i> as they would an <a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a> returned from OleGetClipboard.

When a range covers multiple regions, the method should be called on each region separately. Otherwise, the method might fail.

By default, text services start and end a temporary composition that covers the range, to ensure that context owners consistently recognize compositions over edited text. If the composition owner rejects a default composition, then the method returns TF_E_COMPOSITION_REJECTED. Default compositions are only created if the caller has not already started one. If the caller has an active composition, the call fails.

To determine in advance whether a context owner supports insertion of a particular object, use <a href="/windows/desktop/api/msctf/nf-msctf-itfqueryembedded-queryinsertembedded">ITfQueryEmbedded::QueryInsertEmbedded</a>.

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfdocumentmgr-createcontext">ITfDocumentMgr::CreateContext
      </a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfeditsession-doeditsession">ITfEditSession::DoEditSession
      </a>



<a href="/windows/desktop/api/msctf/nn-msctf-itfrange">ITfRange</a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfrange-getembedded">ITfRange::GetEmbedded
      </a>



<a href="/windows/desktop/TSF/miscellaneous-framework-constants">Miscellaneous Framework Constants</a>



<a href="/windows/desktop/TSF/text-stores">Text Stores</a>