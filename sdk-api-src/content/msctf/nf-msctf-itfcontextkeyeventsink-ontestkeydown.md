---
UID: NF:msctf.ITfContextKeyEventSink.OnTestKeyDown
title: ITfContextKeyEventSink::OnTestKeyDown
author: windows-sdk-content
description: ITfContextKeyEventSink::OnTestKeyDown method
old-location: tsf\itfcontextkeyeventsink_ontestkeydown.htm
tech.root: TSF
ms.assetid: 26f22721-6d64-4637-92cd-8c18caa2d95f
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ITfContextKeyEventSink interface [Text Services Framework],OnTestKeyDown method, ITfContextKeyEventSink.OnTestKeyDown, ITfContextKeyEventSink::OnTestKeyDown, OnTestKeyDown, OnTestKeyDown method [Text Services Framework], OnTestKeyDown method [Text Services Framework],ITfContextKeyEventSink interface, _tsf_itfcontextkeyeventsink_ontestkeydown_ref, msctf/ITfContextKeyEventSink::OnTestKeyDown, tsf.itfcontextkeyeventsink_ontestkeydown
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
 - ITfContextKeyEventSink.OnTestKeyDown
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# ITfContextKeyEventSink::OnTestKeyDown


## -description




## -parameters




### -param wParam [in]

Specifies the virtual-key code of the key. For more information about this parameter, see the <i>wParam</i> parameter in <a href="https://msdn.microsoft.com/en-us/library/ms646280(v=VS.85).aspx">WM_KEYDOWN</a>.


### -param lParam [in]

Specifies the repeat count, scan code, extended-key flag, context code, previous key-state flag, and transition-state flag of the key. For more information about this parameter, see the <i>lParam</i> parameter in <a href="https://msdn.microsoft.com/en-us/library/ms646280(v=VS.85).aspx">WM_KEYDOWN</a>.


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




<a href="https://msdn.microsoft.com/26fc5d8a-e24e-414e-a355-c1f89251f6bd">ITfContextKeyEventSink</a>



<a href="https://msdn.microsoft.com/en-us/library/ms646280(v=VS.85).aspx">WM_KEYDOWN</a>
 

 

