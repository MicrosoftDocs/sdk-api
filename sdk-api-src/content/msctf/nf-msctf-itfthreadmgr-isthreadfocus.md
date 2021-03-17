---
UID: NF:msctf.ITfThreadMgr.IsThreadFocus
title: ITfThreadMgr::IsThreadFocus (msctf.h)
description: ITfThreadMgr::IsThreadFocus method
helpviewer_keywords: ["ITfThreadMgr interface [Text Services Framework]","IsThreadFocus method","ITfThreadMgr.IsThreadFocus","ITfThreadMgr::IsThreadFocus","IsThreadFocus","IsThreadFocus method [Text Services Framework]","IsThreadFocus method [Text Services Framework]","ITfThreadMgr interface","_tsf_itfthreadmgr_isthreadfocus_ref","msctf/ITfThreadMgr::IsThreadFocus","tsf.itfthreadmgr_isthreadfocus"]
old-location: tsf\itfthreadmgr_isthreadfocus.htm
tech.root: TSF
ms.assetid: fa753a4d-4f78-45e0-b711-c294adbb307a
ms.date: 12/05/2018
ms.keywords: ITfThreadMgr interface [Text Services Framework],IsThreadFocus method, ITfThreadMgr.IsThreadFocus, ITfThreadMgr::IsThreadFocus, IsThreadFocus, IsThreadFocus method [Text Services Framework], IsThreadFocus method [Text Services Framework],ITfThreadMgr interface, _tsf_itfthreadmgr_isthreadfocus_ref, msctf/ITfThreadMgr::IsThreadFocus, tsf.itfthreadmgr_isthreadfocus
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
 - ITfThreadMgr::IsThreadFocus
 - msctf/ITfThreadMgr::IsThreadFocus
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
 - ITfThreadMgr.IsThreadFocus
---

# ITfThreadMgr::IsThreadFocus


## -description

Determines if the calling thread has the TSF input focus.

## -parameters

### -param pfThreadFocus [out]

Pointer to a BOOL that receives a value that indicates if the calling thread has input focus. This parameter receives a nonzero value if the calling thread has the focus or zero otherwise.

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
<i>pfThreadFocus</i> is invalid.

</td>
</tr>
</table>

