---
UID: NF:msctf.ITfKeyEventSink.OnKeyUp
title: ITfKeyEventSink::OnKeyUp (msctf.h)
description: ITfKeyEventSink::OnKeyUp method
helpviewer_keywords: ["ITfKeyEventSink interface [Text Services Framework]","OnKeyUp method","ITfKeyEventSink.OnKeyUp","ITfKeyEventSink::OnKeyUp","OnKeyUp","OnKeyUp method [Text Services Framework]","OnKeyUp method [Text Services Framework]","ITfKeyEventSink interface","_tsf_itfkeyeventsink_onkeyup_ref","msctf/ITfKeyEventSink::OnKeyUp","tsf.itfkeyeventsink_onkeyup"]
old-location: tsf\itfkeyeventsink_onkeyup.htm
tech.root: TSF
ms.assetid: 5718a15b-985e-4286-a963-cee513e7550c
ms.date: 12/05/2018
ms.keywords: ITfKeyEventSink interface [Text Services Framework],OnKeyUp method, ITfKeyEventSink.OnKeyUp, ITfKeyEventSink::OnKeyUp, OnKeyUp, OnKeyUp method [Text Services Framework], OnKeyUp method [Text Services Framework],ITfKeyEventSink interface, _tsf_itfkeyeventsink_onkeyup_ref, msctf/ITfKeyEventSink::OnKeyUp, tsf.itfkeyeventsink_onkeyup
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
 - ITfKeyEventSink::OnKeyUp
 - msctf/ITfKeyEventSink::OnKeyUp
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
 - ITfKeyEventSink.OnKeyUp
---

# ITfKeyEventSink::OnKeyUp


## -description

Called when a key up event occurs.

## -parameters

### -param pic [in]

Pointer to the input context that receives the key event.

### -param wParam [in]

Specifies the virtual-key code of the key. For more information about this parameter, see the <i>wParam</i> parameter in <a href="/windows/desktop/inputdev/wm-keyup">WM_KEYUP</a>.

### -param lParam [in]

Specifies the repeat count, scan code, extended-key flag, context code, previous key-state flag, and transition-state flag of the key. For more information about this parameter, see the <i>lParam</i> parameter in <a href="/windows/desktop/inputdev/wm-keyup">WM_KEYUP</a>.

### -param pfEaten [out]

Pointer to a BOOL that, on exit, indicates if the key event was handled. If this value receives <b>TRUE</b>, the key event was handled. If this value receives <b>FALSE</b>, the key event was not handled.

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

[ITfKeyEventSink interface](nn-msctf-itfkeyeventsink.md), [WM_KEYUP](/windows/win32/inputdev/wm-keyup), [Keyboard Input](/windows/win32/inputdev/keyboard-input)
