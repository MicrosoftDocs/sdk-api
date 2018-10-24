---
UID: NF:msctf.ITfContextKeyEventSink.OnTestKeyUp
title: ITfContextKeyEventSink::OnTestKeyUp
author: windows-sdk-content
description: ITfContextKeyEventSink::OnTestKeyUp method
old-location: tsf\itfcontextkeyeventsink_ontestkeyup.htm
tech.root: TSF
ms.assetid: 0905b5e0-077e-4867-affa-9b2b542ec53d
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: ITfContextKeyEventSink interface [Text Services Framework],OnTestKeyUp method, ITfContextKeyEventSink.OnTestKeyUp, ITfContextKeyEventSink::OnTestKeyUp, OnTestKeyUp, OnTestKeyUp method [Text Services Framework], OnTestKeyUp method [Text Services Framework],ITfContextKeyEventSink interface, _tsf_itfcontextkeyeventsink_ontestkeyup_ref, msctf/ITfContextKeyEventSink::OnTestKeyUp, tsf.itfcontextkeyeventsink_ontestkeyup
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mscandui.dll
api_name:
 - ITfContextKeyEventSink.OnTestKeyUp
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# ITfContextKeyEventSink::OnTestKeyUp


## -description




## -parameters




### -param wParam [in]

Specifies the virtual-key code of the key. For more information about this parameter, see the <i>wParam</i> parameter in <a href="_win32_wm_keyup">WM_KEYUP</a>.


### -param lParam [in]

Specifies the repeat count, scan code, extended-key flag, context code, previous key-state flag, and transition-state flag of the key. For more information about this parameter, see the <i>lParam</i> parameter in <a href="_win32_wm_keyup">WM_KEYUP</a>.


### -param pfEaten [out]

Pointer to a BOOL value that, on exit, indicates if the key event is handled. If this value receives <b>TRUE</b>, the key event is handled. If this value receives <b>FALSE</b>, the key event would is not handled.


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




<a href="https://msdn.microsoft.com/26fc5d8a-e24e-414e-a355-c1f89251f6bd">ITfContextKeyEventSink</a>



<a href="_win32_wm_keyup">WM_KEYUP</a>
 

 

