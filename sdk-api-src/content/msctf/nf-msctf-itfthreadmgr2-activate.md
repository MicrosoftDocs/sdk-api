---
UID: NF:msctf.ITfThreadMgr2.Activate
title: ITfThreadMgr2::Activate (msctf.h)
description: Activates TSF for the calling thread.
helpviewer_keywords: ["Activate","Activate method [Text Services Framework]","Activate method [Text Services Framework]","ITfThreadMgr2 interface","ITfThreadMgr2 interface [Text Services Framework]","Activate method","ITfThreadMgr2.Activate","ITfThreadMgr2::Activate","msctf/ITfThreadMgr2::Activate","tsf.itfthreadmgr2_activate"]
old-location: tsf\itfthreadmgr2_activate.htm
tech.root: TSF
ms.assetid: FD1548F5-15F6-4BBC-A7D1-B0F4B881D9F8
ms.date: 12/05/2018
ms.keywords: Activate, Activate method [Text Services Framework], Activate method [Text Services Framework],ITfThreadMgr2 interface, ITfThreadMgr2 interface [Text Services Framework],Activate method, ITfThreadMgr2.Activate, ITfThreadMgr2::Activate, msctf/ITfThreadMgr2::Activate, tsf.itfthreadmgr2_activate
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
 - ITfThreadMgr2::Activate
 - msctf/ITfThreadMgr2::Activate
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
 - ITfThreadMgr2.Activate
---

# ITfThreadMgr2::Activate


## -description

 Activates TSF for the calling thread.

## -parameters

### -param ptid [out]

Pointer to a <a href="/windows/desktop/TSF/tfclientid">TfClientId</a> value that receives a client identifier.

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
<i>ptid</i> is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
This method was called while the thread was deactivated.

</td>
</tr>
</table>

## -remarks

This method can be called more than once from a thread, but each call must be matched with a corresponding call to <a href="/windows/desktop/api/msctf/nf-msctf-itfthreadmgr2-deactivate">Deactivate</a> from the same thread.

## -see-also

<a href="/windows/desktop/api/msctf/nn-msctf-itfthreadmgr2">ITfThreadMgr2</a>