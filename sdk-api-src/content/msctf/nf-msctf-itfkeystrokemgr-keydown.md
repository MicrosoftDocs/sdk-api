---
UID: NF:msctf.ITfKeystrokeMgr.KeyDown
title: ITfKeystrokeMgr::KeyDown (msctf.h)
description: ITfKeystrokeMgr::KeyDown method
helpviewer_keywords: ["ITfKeystrokeMgr interface [Text Services Framework]","KeyDown method","ITfKeystrokeMgr.KeyDown","ITfKeystrokeMgr::KeyDown","KeyDown","KeyDown method [Text Services Framework]","KeyDown method [Text Services Framework]","ITfKeystrokeMgr interface","_tsf_itfkeystrokemgr_keydown_ref","msctf/ITfKeystrokeMgr::KeyDown","tsf.itfkeystrokemgr_keydown"]
old-location: tsf\itfkeystrokemgr_keydown.htm
tech.root: TSF
ms.assetid: 6eb4ad91-9431-4dec-b6cb-e58707318095
ms.date: 12/05/2018
ms.keywords: ITfKeystrokeMgr interface [Text Services Framework],KeyDown method, ITfKeystrokeMgr.KeyDown, ITfKeystrokeMgr::KeyDown, KeyDown, KeyDown method [Text Services Framework], KeyDown method [Text Services Framework],ITfKeystrokeMgr interface, _tsf_itfkeystrokemgr_keydown_ref, msctf/ITfKeystrokeMgr::KeyDown, tsf.itfkeystrokemgr_keydown
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
 - ITfKeystrokeMgr::KeyDown
 - msctf/ITfKeystrokeMgr::KeyDown
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
 - ITfKeystrokeMgr.KeyDown
---

# ITfKeystrokeMgr::KeyDown


## -description

Passes a key down event to the keystroke manager.

## -parameters

### -param wParam [in]

Specifies the virtual-key code of the key. For more information about this parameter, see the <i>wParam</i> parameter in <a href="/windows/desktop/inputdev/wm-keydown">WM_KEYDOWN</a>.

### -param lParam [in]

Specifies the repeat count, scan code, extended-key flag, context code, previous key-state flag, and transition-state flag of the key. For more information about this parameter, see the <i>lParam</i> parameter in <a href="/windows/desktop/inputdev/wm-keydown">WM_KEYDOWN</a>.

### -param pfEaten [out]

Pointer to a BOOL that, on exit, indicates if the key event was handled. If this value receives <b>TRUE</b>, the key event was handled and the event should not be forwarded to the application. If this value is <b>FALSE</b>, the key event was not handled and the event should be forwarded to the application.

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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
There are no key event sinks installed.

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
</table>

## -remarks

If this method is successful and <i>pfEaten</i> receives <b>TRUE</b>, the application should not process the key down event. If this method does not return S_OK or <i>pfEaten</i> receives <b>FALSE</b>, the application should process the key down event. The following is an example of how this is implemented.


``` syntax

if(msg.message == WM_KEYDOWN)
{
    if( pKeyboardMgr->TestKeyDown(msg.wParam, msg.lParam, &fEaten) == S_OK 
        && fEaten 
        && pKeyboardMgr->KeyDown(msg.wParam, msg.lParam, &fEaten) == S_OK 
        && fEaten)
    {
        //The key was handled by the keystroke manager or a TSF text service. Do not pass the key to the application. 
        continue;
    }
    else
    {
        //Let the application process the key. 
    }
}

```

If the keystroke manager does not handle the key event, it passes the key event to TSF text services by calling the TSF text service <a href="/windows/desktop/api/msctf/nf-msctf-itfkeyeventsink-onkeydown">ITfKeyEventSink::OnKeyDown</a> method.

## -see-also

- <a href="/windows/desktop/api/msctf/nf-msctf-itfkeyeventsink-onkeydown">ITfKeyEventSink::OnKeyDown</a>
- <a href="/windows/desktop/api/msctf/nn-msctf-itfkeystrokemgr">ITfKeystrokeMgr</a>
- <a href="/windows/desktop/api/msctf/nf-msctf-itfkeystrokemgr-keyup">ITfKeystrokeMgr::KeyUp</a>
- <a href="/windows/desktop/api/msctf/nf-msctf-itfkeystrokemgr-testkeydown">ITfKeystrokeMgr::TestKeyDown</a>
- <a href="/windows/desktop/inputdev/wm-keydown">WM_KEYDOWN</a>
- <a href="/windows/desktop/inputdev/keyboard-input">Keyboard Input</a>