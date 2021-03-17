---
UID: NF:msctf.ITfRange.GetFormattedText
title: ITfRange::GetFormattedText (msctf.h)
description: The ITfRange::GetFormattedText method obtains formatted content contained within a range of text. The content is packaged in an object that supports the IDataObject interface.
helpviewer_keywords: ["GetFormattedText","GetFormattedText method [Text Services Framework]","GetFormattedText method [Text Services Framework]","ITfRange interface","ITfRange interface [Text Services Framework]","GetFormattedText method","ITfRange.GetFormattedText","ITfRange::GetFormattedText","_tsf_itfrange_getformattedtext_ref","msctf/ITfRange::GetFormattedText","tsf.itfrange_getformattedtext"]
old-location: tsf\itfrange_getformattedtext.htm
tech.root: TSF
ms.assetid: 8da4cb21-7097-4ba9-a63b-3699ef267776
ms.date: 12/05/2018
ms.keywords: GetFormattedText, GetFormattedText method [Text Services Framework], GetFormattedText method [Text Services Framework],ITfRange interface, ITfRange interface [Text Services Framework],GetFormattedText method, ITfRange.GetFormattedText, ITfRange::GetFormattedText, _tsf_itfrange_getformattedtext_ref, msctf/ITfRange::GetFormattedText, tsf.itfrange_getformattedtext
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
 - ITfRange::GetFormattedText
 - msctf/ITfRange::GetFormattedText
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
 - ITfRange.GetFormattedText
---

# ITfRange::GetFormattedText


## -description

The <b>ITfRange::GetFormattedText</b> method obtains formatted content contained within a range of text. The content is packaged in an object that supports the <a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a> interface.

## -parameters

### -param ec [in]

Edit cookie obtained from <a href="/windows/desktop/api/msctf/nf-msctf-itfdocumentmgr-createcontext">ITfDocumentMgr::CreateContext</a> or <a href="/windows/desktop/api/msctf/nf-msctf-itfeditsession-doeditsession">ITfEditSession::DoEditSession</a>.

### -param ppDataObject [out]

Pointer to an <b>IDataObject</b> pointer that receives an object that contains the formatted content. The formatted content is obtained using a STGMEDIUM global memory handle.

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
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The context owner does not support exporting formatted text as an <b>IDataObject</b> object.

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
</table>

## -remarks

The format and storage type of the <b>IDataObject</b> are determined by the application to which the range belongs.

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfdocumentmgr-createcontext">ITfDocumentMgr::CreateContext
      </a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfeditsession-doeditsession">ITfEditSession::DoEditSession
      </a>



<a href="/windows/desktop/api/msctf/nn-msctf-itfrange">ITfRange</a>



<a href="/windows/desktop/TSF/text-stores">Text Stores</a>