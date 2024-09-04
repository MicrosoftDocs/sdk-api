---
UID: NF:msctf.ITfKeystrokeMgr.KeyUp
title: ITfKeystrokeMgr::KeyUp (msctf.h)
description: ITfKeystrokeMgr::KeyUp method
helpviewer_keywords: ["ITfKeystrokeMgr interface [Text Services Framework]","KeyUp method","ITfKeystrokeMgr.KeyUp","ITfKeystrokeMgr::KeyUp","KeyUp","KeyUp method [Text Services Framework]","KeyUp method [Text Services Framework]","ITfKeystrokeMgr interface","_tsf_itfkeystrokemgr_keyup_ref","msctf/ITfKeystrokeMgr::KeyUp","tsf.itfkeystrokemgr_keyup"]
old-location: tsf\itfkeystrokemgr_keyup.htm
tech.root: TSF
ms.assetid: 14415de3-f397-4866-b7d1-167c0931a80c
ms.date: 12/05/2018
ms.keywords: ITfKeystrokeMgr interface [Text Services Framework],KeyUp method, ITfKeystrokeMgr.KeyUp, ITfKeystrokeMgr::KeyUp, KeyUp, KeyUp method [Text Services Framework], KeyUp method [Text Services Framework],ITfKeystrokeMgr interface, _tsf_itfkeystrokemgr_keyup_ref, msctf/ITfKeystrokeMgr::KeyUp, tsf.itfkeystrokemgr_keyup
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
 - ITfKeystrokeMgr::KeyUp
 - msctf/ITfKeystrokeMgr::KeyUp
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
 - ITfKeystrokeMgr.KeyUp
---

# ITfKeystrokeMgr::KeyUp


## -description

Passes a key up event to the keystroke manager.

## -parameters

### -param wParam [in]

Specifies the virtual-key code of the key. For more information about this parameter, see the <i>wParam</i> parameter in <a href="/windows/desktop/inputdev/wm-keyup">WM_KEYUP</a>.

### -param lParam [in]

Specifies the repeat count, scan code, extended-key flag, context code, previous key-state flag, and transition-state flag of the key. For more information about this parameter, see the <i>lParam</i> parameter in <a href="/windows/desktop/inputdev/wm-keyup">WM_KEYUP</a>.

### -param pfEaten [out]

Pointer to a BOOL that, on exit, indicates if the key event will be handled. If this value receives <b>TRUE</b>, the key event would be handled and the event should not be forwarded to the application. If this value is <b>FALSE</b>, the key event would not be handled and the event should be forwarded to the application.

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
No key event sinks are installed.

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

if(msg.message == WM_KEYUP)
{
    if( pKeyboardMgr->TestKeyUp(msg.wParam, msg.lParam, &fEaten) == S_OK 
        && fEaten 
        && pKeyboardMgr->KeyUp(msg.wParam, msg.lParam, &fEaten) == S_OK 
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

If the keystroke manager does not handle the key event, it passes the key event to the text services by a call to the text service <a href="/windows/desktop/api/msctf/nf-msctf-itfkeyeventsink-onkeyup">ITfKeyEventSink::OnKeyUp</a> method.

## -see-also

- <a href="/windows/desktop/api/msctf/nf-msctf-itfkeyeventsink-onkeyup">ITfKeyEventSink::OnKeyUp</a>
- <a href="/windows/desktop/api/msctf/nn-msctf-itfkeystrokemgr">ITfKeystrokeMgr</a>
- <a href="/windows/desktop/api/msctf/nf-msctf-itfkeystrokemgr-keydown">ITfKeystrokeMgr::KeyDown</a>
- <a href="/windows/desktop/api/msctf/nf-msctf-itfkeystrokemgr-testkeyup">ITfKeystrokeMgr::TestKeyUp</a>
- <a href="/windows/desktop/inputdev/wm-keyup">WM_KEYUP</a>
- <a href="/windows/desktop/inputdev/keyboard-input">Keyboard Input</a>