---
UID: NF:msctf.ITfKeyTraceEventSink.OnKeyTraceUp
title: ITfKeyTraceEventSink::OnKeyTraceUp (msctf.h)
description: ITfKeyTraceEventSink::OnKeyTraceUp method
helpviewer_keywords: ["ITfKeyTraceEventSink interface [Text Services Framework]","OnKeyTraceUp method","ITfKeyTraceEventSink.OnKeyTraceUp","ITfKeyTraceEventSink::OnKeyTraceUp","OnKeyTraceUp","OnKeyTraceUp method [Text Services Framework]","OnKeyTraceUp method [Text Services Framework]","ITfKeyTraceEventSink interface","_tsf_itfkeytraceeventsink_onkeytraceup_ref","msctf/ITfKeyTraceEventSink::OnKeyTraceUp","tsf.itfkeytraceeventsink_onkeytraceup"]
old-location: tsf\itfkeytraceeventsink_onkeytraceup.htm
tech.root: TSF
ms.assetid: 5b86de82-2c27-4824-91bb-39001b5a19e7
ms.date: 12/05/2018
ms.keywords: ITfKeyTraceEventSink interface [Text Services Framework],OnKeyTraceUp method, ITfKeyTraceEventSink.OnKeyTraceUp, ITfKeyTraceEventSink::OnKeyTraceUp, OnKeyTraceUp, OnKeyTraceUp method [Text Services Framework], OnKeyTraceUp method [Text Services Framework],ITfKeyTraceEventSink interface, _tsf_itfkeytraceeventsink_onkeytraceup_ref, msctf/ITfKeyTraceEventSink::OnKeyTraceUp, tsf.itfkeytraceeventsink_onkeytraceup
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
 - ITfKeyTraceEventSink::OnKeyTraceUp
 - msctf/ITfKeyTraceEventSink::OnKeyTraceUp
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
 - ITfKeyTraceEventSink.OnKeyTraceUp
---

# ITfKeyTraceEventSink::OnKeyTraceUp


## -description

Called when a key up event occurs.

## -parameters

### -param wParam [in]

The WPARAM of the key event. For more information about this parameter, see the <i>wParam</i> parameter in <a href="/windows/desktop/inputdev/wm-keyup">WM_KEYUP</a>.

### -param lParam [in]

The LPARAM of the key event. For more information about this parameter, see the <i>lParam</i> parameter in <a href="/windows/desktop/inputdev/wm-keyup">WM_KEYUP</a>.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

- <a href="/windows/desktop/api/msctf/nn-msctf-itfkeytraceeventsink">ITfKeyTraceEventSink</a>
- <a href="/windows/desktop/inputdev/wm-keyup">WM_KEYUP</a>
- <a href="/windows/desktop/inputdev/keyboard-input">Keyboard Input</a>