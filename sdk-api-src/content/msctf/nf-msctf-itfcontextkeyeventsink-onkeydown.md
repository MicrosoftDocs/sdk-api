---
UID: NF:msctf.ITfContextKeyEventSink.OnKeyDown
title: ITfContextKeyEventSink::OnKeyDown (msctf.h)
description: ITfContextKeyEventSink::OnKeyDown method
helpviewer_keywords: ["ITfContextKeyEventSink interface [Text Services Framework]","OnKeyDown method","ITfContextKeyEventSink.OnKeyDown","ITfContextKeyEventSink::OnKeyDown","OnKeyDown","OnKeyDown method [Text Services Framework]","OnKeyDown method [Text Services Framework]","ITfContextKeyEventSink interface","_tsf_itfcontextkeyeventsink_onkeydown_ref","msctf/ITfContextKeyEventSink::OnKeyDown","tsf.itfcontextkeyeventsink_onkeydown"]
old-location: tsf\itfcontextkeyeventsink_onkeydown.htm
tech.root: TSF
ms.assetid: 684d3c01-fa95-4a19-b5fb-48a62315ce2f
ms.date: 12/05/2018
ms.keywords: ITfContextKeyEventSink interface [Text Services Framework],OnKeyDown method, ITfContextKeyEventSink.OnKeyDown, ITfContextKeyEventSink::OnKeyDown, OnKeyDown, OnKeyDown method [Text Services Framework], OnKeyDown method [Text Services Framework],ITfContextKeyEventSink interface, _tsf_itfcontextkeyeventsink_onkeydown_ref, msctf/ITfContextKeyEventSink::OnKeyDown, tsf.itfcontextkeyeventsink_onkeydown
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
req.dll: Mscandui.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - ITfContextKeyEventSink::OnKeyDown
 - msctf/ITfContextKeyEventSink::OnKeyDown
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mscandui.dll
api_name:
 - ITfContextKeyEventSink.OnKeyDown
---

# ITfContextKeyEventSink::OnKeyDown


## -description

Called when a key down event occurs.

## -parameters

### -param wParam [in]

Specifies the virtual-key code of the key. For more information about this parameter, see the <i>wParam</i> parameter in <a href="/windows/desktop/inputdev/wm-keydown">WM_KEYDOWN</a>.

### -param lParam [in]

Specifies the repeat count, scan code, extended-key flag, context code, previous key-state flag, and transition-state flag of the key. For more information about this parameter, see the <i>lParam</i> parameter in <a href="/windows/desktop/inputdev/wm-keydown">WM_KEYDOWN</a>.

### -param pfEaten [out]

Pointer to a BOOL value that, on exit, indicates if the key event is handled. If this value receives <b>TRUE</b>, the key event is handled. If this value is <b>FALSE</b>, the key event is not handled.

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
</table>

## -see-also

[ITfContextKeyEventSink interface](nn-msctf-itfcontextkeyeventsink.md), [WM_KEYDOWN](/windows/desktop/inputdev/wm-keydown), <a href="/windows/desktop/inputdev/keyboard-input">Keyboard Input</a>
