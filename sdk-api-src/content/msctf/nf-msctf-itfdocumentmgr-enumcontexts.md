---
UID: NF:msctf.ITfDocumentMgr.EnumContexts
title: ITfDocumentMgr::EnumContexts (msctf.h)
description: ITfDocumentMgr::EnumContexts method
helpviewer_keywords: ["EnumContexts","EnumContexts method [Text Services Framework]","EnumContexts method [Text Services Framework]","ITfDocumentMgr interface","ITfDocumentMgr interface [Text Services Framework]","EnumContexts method","ITfDocumentMgr.EnumContexts","ITfDocumentMgr::EnumContexts","_tsf_itfdocumentmgr_enumcontexts_ref","msctf/ITfDocumentMgr::EnumContexts","tsf.itfdocumentmgr_enumcontexts"]
old-location: tsf\itfdocumentmgr_enumcontexts.htm
tech.root: TSF
ms.assetid: 0656301a-9e24-4b13-bc39-7d9085c0d6f2
ms.date: 12/05/2018
ms.keywords: EnumContexts, EnumContexts method [Text Services Framework], EnumContexts method [Text Services Framework],ITfDocumentMgr interface, ITfDocumentMgr interface [Text Services Framework],EnumContexts method, ITfDocumentMgr.EnumContexts, ITfDocumentMgr::EnumContexts, _tsf_itfdocumentmgr_enumcontexts_ref, msctf/ITfDocumentMgr::EnumContexts, tsf.itfdocumentmgr_enumcontexts
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
 - ITfDocumentMgr::EnumContexts
 - msctf/ITfDocumentMgr::EnumContexts
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
 - ITfDocumentMgr.EnumContexts
---

# ITfDocumentMgr::EnumContexts


## -description

Obtains a context enumerator.

## -parameters

### -param ppEnum [out]

Address of an <a href="/windows/desktop/api/msctf/nn-msctf-ienumtfcontexts">IEnumTfContexts</a> pointer that receives the enumerator.

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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
A memory allocation error occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The enumerator cannot be initialized.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/msctf/nn-msctf-ienumtfcontexts">IEnumTfContexts
      </a>



<a href="/windows/desktop/api/msctf/nn-msctf-itfdocumentmgr">ITfDocumentMgr</a>