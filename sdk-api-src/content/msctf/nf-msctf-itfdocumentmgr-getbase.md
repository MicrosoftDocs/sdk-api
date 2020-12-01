---
UID: NF:msctf.ITfDocumentMgr.GetBase
title: ITfDocumentMgr::GetBase (msctf.h)
description: ITfDocumentMgr::GetBase method
helpviewer_keywords: ["GetBase","GetBase method [Text Services Framework]","GetBase method [Text Services Framework]","ITfDocumentMgr interface","ITfDocumentMgr interface [Text Services Framework]","GetBase method","ITfDocumentMgr.GetBase","ITfDocumentMgr::GetBase","_tsf_itfdocumentmgr_getbase_ref","msctf/ITfDocumentMgr::GetBase","tsf.itfdocumentmgr_getbase"]
old-location: tsf\itfdocumentmgr_getbase.htm
tech.root: TSF
ms.assetid: 71248c77-7440-412c-b565-39c04108b98b
ms.date: 12/05/2018
ms.keywords: GetBase, GetBase method [Text Services Framework], GetBase method [Text Services Framework],ITfDocumentMgr interface, ITfDocumentMgr interface [Text Services Framework],GetBase method, ITfDocumentMgr.GetBase, ITfDocumentMgr::GetBase, _tsf_itfdocumentmgr_getbase_ref, msctf/ITfDocumentMgr::GetBase, tsf.itfdocumentmgr_getbase
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
 - ITfDocumentMgr::GetBase
 - msctf/ITfDocumentMgr::GetBase
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
 - ITfDocumentMgr.GetBase
---

# ITfDocumentMgr::GetBase


## -description

Obtains the context at the base of the context stack.

## -parameters

### -param ppic [out]

Address of an <a href="/windows/desktop/api/msctf/nn-msctf-itfcontext">ITfContext</a> pointer that receives the context.

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
<i>ppic</i> is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
A memory allocation error occurred.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/msctf/nn-msctf-itfcontext">ITfContext
      </a>



<a href="/windows/desktop/api/msctf/nn-msctf-itfdocumentmgr">ITfDocumentMgr</a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfdocumentmgr-gettop">ITfDocumentMgr::GetTop
      </a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfdocumentmgr-push">ITfDocumentMgr::Push
      </a>