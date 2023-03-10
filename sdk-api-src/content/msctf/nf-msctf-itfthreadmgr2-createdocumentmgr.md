---
UID: NF:msctf.ITfThreadMgr2.CreateDocumentMgr
title: ITfThreadMgr2::CreateDocumentMgr (msctf.h)
description: Creates a document manager object.
helpviewer_keywords: ["CreateDocumentMgr","CreateDocumentMgr method [Text Services Framework]","CreateDocumentMgr method [Text Services Framework]","ITfThreadMgr2 interface","ITfThreadMgr2 interface [Text Services Framework]","CreateDocumentMgr method","ITfThreadMgr2.CreateDocumentMgr","ITfThreadMgr2::CreateDocumentMgr","msctf/ITfThreadMgr2::CreateDocumentMgr","tsf.itfthreadmgr2_createdocumentmgr"]
old-location: tsf\itfthreadmgr2_createdocumentmgr.htm
tech.root: TSF
ms.assetid: 4B19EA80-9F42-4FFF-AB3D-4D0B5B2174F8
ms.date: 12/05/2018
ms.keywords: CreateDocumentMgr, CreateDocumentMgr method [Text Services Framework], CreateDocumentMgr method [Text Services Framework],ITfThreadMgr2 interface, ITfThreadMgr2 interface [Text Services Framework],CreateDocumentMgr method, ITfThreadMgr2.CreateDocumentMgr, ITfThreadMgr2::CreateDocumentMgr, msctf/ITfThreadMgr2::CreateDocumentMgr, tsf.itfthreadmgr2_createdocumentmgr
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITfThreadMgr2::CreateDocumentMgr
 - msctf/ITfThreadMgr2::CreateDocumentMgr
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msctf.h
api_name:
 - ITfThreadMgr2.CreateDocumentMgr
---

# ITfThreadMgr2::CreateDocumentMgr


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

<a href="/windows/desktop/api/msctf/nn-msctf-itfthreadmgr2">ITfThreadMgr2</a>