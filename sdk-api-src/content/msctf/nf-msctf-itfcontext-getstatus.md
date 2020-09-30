---
UID: NF:msctf.ITfContext.GetStatus
title: ITfContext::GetStatus (msctf.h)
description: ITfContext::GetStatus method
helpviewer_keywords: ["GetStatus","GetStatus method [Text Services Framework]","GetStatus method [Text Services Framework]","ITfContext interface","ITfContext interface [Text Services Framework]","GetStatus method","ITfContext.GetStatus","ITfContext::GetStatus","_tsf_itfcontext_getstatus_ref","msctf/ITfContext::GetStatus","tsf.itfcontext_getstatus"]
old-location: tsf\itfcontext_getstatus.htm
tech.root: TSF
ms.assetid: a1f193b0-fcfc-4db6-90e9-61d528b08672
ms.date: 12/05/2018
ms.keywords: GetStatus, GetStatus method [Text Services Framework], GetStatus method [Text Services Framework],ITfContext interface, ITfContext interface [Text Services Framework],GetStatus method, ITfContext.GetStatus, ITfContext::GetStatus, _tsf_itfcontext_getstatus_ref, msctf/ITfContext::GetStatus, tsf.itfcontext_getstatus
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
 - ITfContext::GetStatus
 - msctf/ITfContext::GetStatus
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
 - ITfContext.GetStatus
---

# ITfContext::GetStatus


## -description

Obtains the document status.

## -parameters

### -param pdcs [out]

Pointer to a <a href="/previous-versions/windows/desktop/legacy/ms629192(v=vs.85)">TF_STATUS</a> structure that receives the document status data.

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
<dt><b>TF_E_DISCONNECTED</b></dt>
</dl>
</td>
<td width="60%">
The context is not on a document stack.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>pdcs</i> is invalid.

</td>
</tr>
</table>

## -see-also

[ITfContext interface](nn-msctf-itfcontext.md), [TF_STATUS](/previous-versions/windows/desktop/legacy/ms629192(v=vs.85))