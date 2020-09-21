---
UID: NF:msctf.ITfKeystrokeMgr.UnadviseKeyEventSink
title: ITfKeystrokeMgr::UnadviseKeyEventSink (msctf.h)
description: ITfKeystrokeMgr::UnadviseKeyEventSink method
helpviewer_keywords: ["ITfKeystrokeMgr interface [Text Services Framework]","UnadviseKeyEventSink method","ITfKeystrokeMgr.UnadviseKeyEventSink","ITfKeystrokeMgr::UnadviseKeyEventSink","UnadviseKeyEventSink","UnadviseKeyEventSink method [Text Services Framework]","UnadviseKeyEventSink method [Text Services Framework]","ITfKeystrokeMgr interface","_tsf_itfkeystrokemgr_unadvisekeyeventsink_ref","msctf/ITfKeystrokeMgr::UnadviseKeyEventSink","tsf.itfkeystrokemgr_unadvisekeyeventsink"]
old-location: tsf\itfkeystrokemgr_unadvisekeyeventsink.htm
tech.root: TSF
ms.assetid: 72250972-0a0b-4e83-8603-0fb5adc9a2c9
ms.date: 12/05/2018
ms.keywords: ITfKeystrokeMgr interface [Text Services Framework],UnadviseKeyEventSink method, ITfKeystrokeMgr.UnadviseKeyEventSink, ITfKeystrokeMgr::UnadviseKeyEventSink, UnadviseKeyEventSink, UnadviseKeyEventSink method [Text Services Framework], UnadviseKeyEventSink method [Text Services Framework],ITfKeystrokeMgr interface, _tsf_itfkeystrokemgr_unadvisekeyeventsink_ref, msctf/ITfKeystrokeMgr::UnadviseKeyEventSink, tsf.itfkeystrokemgr_unadvisekeyeventsink
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
 - ITfKeystrokeMgr::UnadviseKeyEventSink
 - msctf/ITfKeystrokeMgr::UnadviseKeyEventSink
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
 - ITfKeystrokeMgr.UnadviseKeyEventSink
---

# ITfKeystrokeMgr::UnadviseKeyEventSink


## -description

Removes a key event sink.

## -parameters

### -param tid [in]

Identifier of the client that owns the key event sink. This value was passed when the advise sink was installed using <a href="/windows/desktop/api/msctf/nf-msctf-itfkeystrokemgr-advisekeyeventsink">ITfKeystrokeMgr::AdviseKeyEventSink</a>.

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
The <i>tid</i> parameter is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CONNECT_E_NOCONNECTION</b></dt>
</dl>
</td>
<td width="60%">
The advise sink identified by <i>tid</i> was not found.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/msctf/nn-msctf-itfkeystrokemgr">ITfKeystrokeMgr</a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfkeystrokemgr-advisekeyeventsink">ITfKeystrokeMgr::AdviseKeyEventSink
      </a>