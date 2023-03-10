---
UID: NF:msctf.ITfKeyTraceEventSink.OnKeyTraceDown
title: ITfKeyTraceEventSink::OnKeyTraceDown (msctf.h)
description: ITfKeyTraceEventSink::OnKeyTraceDown method
helpviewer_keywords: ["ITfKeyTraceEventSink interface [Text Services Framework]","OnKeyTraceDown method","ITfKeyTraceEventSink.OnKeyTraceDown","ITfKeyTraceEventSink::OnKeyTraceDown","OnKeyTraceDown","OnKeyTraceDown method [Text Services Framework]","OnKeyTraceDown method [Text Services Framework]","ITfKeyTraceEventSink interface","_tsf_itfkeytraceeventsink_onkeytracedown_ref","msctf/ITfKeyTraceEventSink::OnKeyTraceDown","tsf.itfkeytraceeventsink_onkeytracedown"]
old-location: tsf\itfkeytraceeventsink_onkeytracedown.htm
tech.root: TSF
ms.assetid: 826b45cd-a1ec-406c-bf7a-685a766484e3
ms.date: 12/05/2018
ms.keywords: ITfKeyTraceEventSink interface [Text Services Framework],OnKeyTraceDown method, ITfKeyTraceEventSink.OnKeyTraceDown, ITfKeyTraceEventSink::OnKeyTraceDown, OnKeyTraceDown, OnKeyTraceDown method [Text Services Framework], OnKeyTraceDown method [Text Services Framework],ITfKeyTraceEventSink interface, _tsf_itfkeytraceeventsink_onkeytracedown_ref, msctf/ITfKeyTraceEventSink::OnKeyTraceDown, tsf.itfkeytraceeventsink_onkeytracedown
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
req.dll: Tiptsf.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - ITfKeyTraceEventSink::OnKeyTraceDown
 - msctf/ITfKeyTraceEventSink::OnKeyTraceDown
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tiptsf.dll
api_name:
 - ITfKeyTraceEventSink.OnKeyTraceDown
---

# ITfKeyTraceEventSink::OnKeyTraceDown


## -description

Called when a key down event occurs.

## -parameters

### -param wParam [in]

The WPARAM of the key event. For more information about this parameter, see the <i>wParam</i> parameter in <a href="/windows/desktop/inputdev/wm-keydown">WM_KEYDOWN</a>.

### -param lParam [in]

The LPARAM of the key event. For more information about this parameter, see the <i>lParam</i> parameter in <a href="/windows/desktop/inputdev/wm-keydown">WM_KEYDOWN</a>.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/msctf/nn-msctf-itfkeytraceeventsink">ITfKeyTraceEventSink</a>
<a href="/windows/desktop/inputdev/wm-keydown">WM_KEYDOWN</a>
<a href="/windows/desktop/inputdev/keyboard-input">Keyboard Input</a>