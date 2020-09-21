---
UID: NF:msctf.ITfThreadMgr.Activate
title: ITfThreadMgr::Activate (msctf.h)
description: ITfThreadMgr::Activate method
helpviewer_keywords: ["Activate","Activate method [Text Services Framework]","Activate method [Text Services Framework]","ITfThreadMgr interface","ITfThreadMgr interface [Text Services Framework]","Activate method","ITfThreadMgr.Activate","ITfThreadMgr::Activate","_tsf_itfthreadmgr_activate_ref","msctf/ITfThreadMgr::Activate","tsf.itfthreadmgr_activate"]
old-location: tsf\itfthreadmgr_activate.htm
tech.root: TSF
ms.assetid: bd9058c0-55b0-4231-a336-7cea4db75c0f
ms.date: 12/05/2018
ms.keywords: Activate, Activate method [Text Services Framework], Activate method [Text Services Framework],ITfThreadMgr interface, ITfThreadMgr interface [Text Services Framework],Activate method, ITfThreadMgr.Activate, ITfThreadMgr::Activate, _tsf_itfthreadmgr_activate_ref, msctf/ITfThreadMgr::Activate, tsf.itfthreadmgr_activate
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
 - ITfThreadMgr::Activate
 - msctf/ITfThreadMgr::Activate
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
 - ITfThreadMgr.Activate
---

# ITfThreadMgr::Activate


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
This method was called while the thread was deactivating.

</td>
</tr>
</table>

## -remarks

This method can be called more than once from a thread, but each call must be matched with a corresponding call to <a href="/windows/desktop/api/msctf/nf-msctf-itfthreadmgr-deactivate">ITfThreadMgr::Deactivate</a> from the same thread.

## -see-also

<a href="/windows/desktop/api/msctf/nn-msctf-itfthreadmgr">ITfThreadMgr</a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfthreadmgr-deactivate">ITfThreadMgr::Deactivate
      </a>



<a href="/windows/desktop/TSF/tfclientid">TfClientId
      </a>