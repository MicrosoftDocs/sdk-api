---
UID: NF:msctf.ITfKeystrokeMgr.AdviseKeyEventSink
title: ITfKeystrokeMgr::AdviseKeyEventSink (msctf.h)
description: ITfKeystrokeMgr::AdviseKeyEventSink method
helpviewer_keywords: ["AdviseKeyEventSink","AdviseKeyEventSink method [Text Services Framework]","AdviseKeyEventSink method [Text Services Framework]","ITfKeystrokeMgr interface","ITfKeystrokeMgr interface [Text Services Framework]","AdviseKeyEventSink method","ITfKeystrokeMgr.AdviseKeyEventSink","ITfKeystrokeMgr::AdviseKeyEventSink","_tsf_itfkeystrokemgr_advisekeyeventsink_ref","msctf/ITfKeystrokeMgr::AdviseKeyEventSink","tsf.itfkeystrokemgr_advisekeyeventsink"]
old-location: tsf\itfkeystrokemgr_advisekeyeventsink.htm
tech.root: TSF
ms.assetid: dfda786a-09f5-412c-878d-0ba0cbbdafe0
ms.date: 12/05/2018
ms.keywords: AdviseKeyEventSink, AdviseKeyEventSink method [Text Services Framework], AdviseKeyEventSink method [Text Services Framework],ITfKeystrokeMgr interface, ITfKeystrokeMgr interface [Text Services Framework],AdviseKeyEventSink method, ITfKeystrokeMgr.AdviseKeyEventSink, ITfKeystrokeMgr::AdviseKeyEventSink, _tsf_itfkeystrokemgr_advisekeyeventsink_ref, msctf/ITfKeystrokeMgr::AdviseKeyEventSink, tsf.itfkeystrokemgr_advisekeyeventsink
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
 - ITfKeystrokeMgr::AdviseKeyEventSink
 - msctf/ITfKeystrokeMgr::AdviseKeyEventSink
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
 - ITfKeystrokeMgr.AdviseKeyEventSink
---

# ITfKeystrokeMgr::AdviseKeyEventSink


## -description

Installs a key event sink to receive keyboard events.

## -parameters

### -param tid [in]

Identifier of the client that owns the key event sink. This value is obtained by a previous call to <a href="/windows/desktop/api/msctf/nf-msctf-itfthreadmgr-activate">ITfThreadMgr::Activate</a>.

### -param pSink [in]

Pointer to a <a href="/windows/desktop/api/msctf/nn-msctf-itfkeyeventsink">ITfKeyEventSink</a> interface.

### -param fForeground [in]

Specifies if this key event sink is made the foreground key event sink. If this is <b>TRUE</b>, this key event sink is made the foreground key event sink. Otherwise, this key event sink does not become the foreground key event sink.

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
One or more parameters are invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CONNECT_E_ADVISELIMIT</b></dt>
</dl>
</td>
<td width="60%">
The client identified by <i>tid</i> has a key event sink installed.

</td>
</tr>
</table>

## -remarks

The foreground key event sink receives all keyboard events. A non-foreground key event sink only receives preserved keys and key events that occur over text that marked owned by the client identifier.

## -see-also

<a href="/windows/desktop/api/msctf/nn-msctf-itfkeyeventsink">ITfKeyEventSink
      </a>



<a href="/windows/desktop/api/msctf/nn-msctf-itfkeystrokemgr">ITfKeystrokeMgr</a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfthreadmgr-activate">ITfThreadMgr::Activate
      </a>