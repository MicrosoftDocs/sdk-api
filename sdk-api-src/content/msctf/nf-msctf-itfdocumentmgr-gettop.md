---
UID: NF:msctf.ITfDocumentMgr.GetTop
title: ITfDocumentMgr::GetTop (msctf.h)
description: ITfDocumentMgr::GetTop method
helpviewer_keywords: ["GetTop","GetTop method [Text Services Framework]","GetTop method [Text Services Framework]","ITfDocumentMgr interface","ITfDocumentMgr interface [Text Services Framework]","GetTop method","ITfDocumentMgr.GetTop","ITfDocumentMgr::GetTop","_tsf_itfdocumentmgr_gettop_ref","msctf/ITfDocumentMgr::GetTop","tsf.itfdocumentmgr_gettop"]
old-location: tsf\itfdocumentmgr_gettop.htm
tech.root: TSF
ms.assetid: 5be7635f-ec27-4892-9cfe-dba31e202510
ms.date: 12/05/2018
ms.keywords: GetTop, GetTop method [Text Services Framework], GetTop method [Text Services Framework],ITfDocumentMgr interface, ITfDocumentMgr interface [Text Services Framework],GetTop method, ITfDocumentMgr.GetTop, ITfDocumentMgr::GetTop, _tsf_itfdocumentmgr_gettop_ref, msctf/ITfDocumentMgr::GetTop, tsf.itfdocumentmgr_gettop
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
 - ITfDocumentMgr::GetTop
 - msctf/ITfDocumentMgr::GetTop
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
 - ITfDocumentMgr.GetTop
---

# ITfDocumentMgr::GetTop


## -description

Obtains the context at the top of the context stack.

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



<a href="/windows/desktop/api/msctf/nf-msctf-itfdocumentmgr-getbase">ITfDocumentMgr::GetBase
      </a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfdocumentmgr-push">ITfDocumentMgr::Push
      </a>