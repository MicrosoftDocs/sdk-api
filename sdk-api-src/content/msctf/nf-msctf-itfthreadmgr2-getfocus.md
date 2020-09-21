---
UID: NF:msctf.ITfThreadMgr2.GetFocus
title: ITfThreadMgr2::GetFocus (msctf.h)
description: Returns the document manager that has the input focus.
helpviewer_keywords: ["GetFocus","GetFocus method [Text Services Framework]","GetFocus method [Text Services Framework]","ITfThreadMgr2 interface","ITfThreadMgr2 interface [Text Services Framework]","GetFocus method","ITfThreadMgr2.GetFocus","ITfThreadMgr2::GetFocus","msctf/ITfThreadMgr2::GetFocus","tsf.itfthreadmgr2_getfocus"]
old-location: tsf\itfthreadmgr2_getfocus.htm
tech.root: TSF
ms.assetid: A4106774-1817-4308-BD7E-C303AED2B576
ms.date: 12/05/2018
ms.keywords: GetFocus, GetFocus method [Text Services Framework], GetFocus method [Text Services Framework],ITfThreadMgr2 interface, ITfThreadMgr2 interface [Text Services Framework],GetFocus method, ITfThreadMgr2.GetFocus, ITfThreadMgr2::GetFocus, msctf/ITfThreadMgr2::GetFocus, tsf.itfthreadmgr2_getfocus
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
 - ITfThreadMgr2::GetFocus
 - msctf/ITfThreadMgr2::GetFocus
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
 - ITfThreadMgr2.GetFocus
---

# ITfThreadMgr2::GetFocus


## -description

Returns the document manager that has the input focus.

## -parameters

### -param ppdimFocus [out]

Pointer to a <a href="/windows/desktop/api/msctf/nn-msctf-itfdocumentmgr">ITfDocumentMgr</a> interface that receives the document manager with the current input focus. Receives <b>NULL</b> if no document manager has the focus.

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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
No document manager has focus. <i>ppdimFocus</i> be set to <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>ppdimFocus</i> is invalid.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/msctf/nn-msctf-itfthreadmgr2">ITfThreadMgr2</a>