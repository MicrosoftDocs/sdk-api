---
UID: NF:msctf.ITfKeyEventSink.OnTestKeyDown
title: ITfKeyEventSink::OnTestKeyDown (msctf.h)
description: ITfKeyEventSink::OnTestKeyDown method
helpviewer_keywords: ["ITfKeyEventSink interface [Text Services Framework]","OnTestKeyDown method","ITfKeyEventSink.OnTestKeyDown","ITfKeyEventSink::OnTestKeyDown","OnTestKeyDown","OnTestKeyDown method [Text Services Framework]","OnTestKeyDown method [Text Services Framework]","ITfKeyEventSink interface","_tsf_itfkeyeventsink_ontestkeydown_ref","msctf/ITfKeyEventSink::OnTestKeyDown","tsf.itfkeyeventsink_ontestkeydown"]
old-location: tsf\itfkeyeventsink_ontestkeydown.htm
tech.root: TSF
ms.assetid: 3d8056ef-c012-4989-91ce-65ae8cd39404
ms.date: 12/05/2018
ms.keywords: ITfKeyEventSink interface [Text Services Framework],OnTestKeyDown method, ITfKeyEventSink.OnTestKeyDown, ITfKeyEventSink::OnTestKeyDown, OnTestKeyDown, OnTestKeyDown method [Text Services Framework], OnTestKeyDown method [Text Services Framework],ITfKeyEventSink interface, _tsf_itfkeyeventsink_ontestkeydown_ref, msctf/ITfKeyEventSink::OnTestKeyDown, tsf.itfkeyeventsink_ontestkeydown
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
 - ITfKeyEventSink::OnTestKeyDown
 - msctf/ITfKeyEventSink::OnTestKeyDown
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
 - ITfKeyEventSink.OnTestKeyDown
---

# ITfKeyEventSink::OnTestKeyDown


## -description

Called to determine if a text service will handle a key down event.

## -parameters

### -param pic [in]

Pointer to the input context that receives the key event.

### -param wParam [in]

Specifies the virtual-key code of the key. For more information about this parameter, see the <i>wParam</i> parameter in <a href="/windows/desktop/inputdev/wm-keydown">WM_KEYDOWN</a>.

### -param lParam [in]

Specifies the repeat count, scan code, extended-key flag, context code, previous key-state flag, and transition-state flag of the key. For more information about this parameter, see the <i>lParam</i> parameter in <a href="/windows/desktop/inputdev/wm-keydown">WM_KEYDOWN</a>.

### -param pfEaten [out]

Pointer to a BOOL that, on exit, indicates if the key event would be handled. If this value receives <b>TRUE</b>, the key event would be handled. If this value is <b>FALSE</b>, the key event would not be handled.

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

<a href="/windows/desktop/api/msctf/nn-msctf-itfkeyeventsink">ITfKeyEventSink</a>, <a href="/windows/desktop/inputdev/wm-keydown">WM_KEYDOWN</a>, <a href="/windows/desktop/inputdev/keyboard-input">Keyboard Input</a>