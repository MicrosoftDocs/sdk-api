---
UID: NF:msctf.ITfThreadMgr.CreateDocumentMgr
title: ITfThreadMgr::CreateDocumentMgr (msctf.h)
description: ITfThreadMgr::CreateDocumentMgr method
helpviewer_keywords: ["CreateDocumentMgr","CreateDocumentMgr method [Text Services Framework]","CreateDocumentMgr method [Text Services Framework]","ITfThreadMgr interface","ITfThreadMgr interface [Text Services Framework]","CreateDocumentMgr method","ITfThreadMgr.CreateDocumentMgr","ITfThreadMgr::CreateDocumentMgr","_tsf_itfthreadmgr_createdocumentmgr_ref","msctf/ITfThreadMgr::CreateDocumentMgr","tsf.itfthreadmgr_createdocumentmgr"]
old-location: tsf\itfthreadmgr_createdocumentmgr.htm
tech.root: TSF
ms.assetid: 0f90a359-61e7-46e5-9d0b-ab6fe24f3136
ms.date: 12/05/2018
ms.keywords: CreateDocumentMgr, CreateDocumentMgr method [Text Services Framework], CreateDocumentMgr method [Text Services Framework],ITfThreadMgr interface, ITfThreadMgr interface [Text Services Framework],CreateDocumentMgr method, ITfThreadMgr.CreateDocumentMgr, ITfThreadMgr::CreateDocumentMgr, _tsf_itfthreadmgr_createdocumentmgr_ref, msctf/ITfThreadMgr::CreateDocumentMgr, tsf.itfthreadmgr_createdocumentmgr
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
 - ITfThreadMgr::CreateDocumentMgr
 - msctf/ITfThreadMgr::CreateDocumentMgr
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
 - ITfThreadMgr.CreateDocumentMgr
---

# ITfThreadMgr::CreateDocumentMgr


## -description

Creates a document manager object.

## -parameters

### -param ppdim [out]

Pointer to an <a href="/windows/desktop/api/msctf/nn-msctf-itfdocumentmgr">ITfDocumentMgr</a> interface that receives the document manager object.

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
<i>ppdim</i> is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
A memory allocation failure occurred.

</td>
</tr>
</table>

## -remarks

The caller must release the document manager when it is no longer required.

## -see-also

<a href="/windows/desktop/api/msctf/nn-msctf-itfdocumentmgr">ITfDocumentMgr
      </a>



<a href="/windows/desktop/api/msctf/nn-msctf-itfthreadmgr">ITfThreadMgr</a>