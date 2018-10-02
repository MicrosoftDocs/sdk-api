---
UID: NF:msctf.ITfKeyEventSink.OnKeyDown
title: ITfKeyEventSink::OnKeyDown
author: windows-sdk-content
description: ITfKeyEventSink::OnKeyDown method
old-location: tsf\itfkeyeventsink_onkeydown.htm
tech.root: TSF
ms.assetid: aceeb367-0963-484b-afae-26a2c4fb24c7
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: ITfKeyEventSink interface [Text Services Framework],OnKeyDown method, ITfKeyEventSink.OnKeyDown, ITfKeyEventSink::OnKeyDown, OnKeyDown, OnKeyDown method [Text Services Framework], OnKeyDown method [Text Services Framework],ITfKeyEventSink interface, _tsf_itfkeyeventsink_onkeydown_ref, msctf/ITfKeyEventSink::OnKeyDown, tsf.itfkeyeventsink_onkeydown
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msctf.dll
api_name:
 - ITfKeyEventSink.OnKeyDown
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# ITfKeyEventSink::OnKeyDown


## -description




## -parameters




### -param pic [in]

Pointer to the input context that receives the key event.


### -param wParam [in]

Specifies the virtual-key code of the key. For more information about this parameter, see the <i>wParam</i> parameter in <a href="https://msdn.microsoft.com/en-us/library/ms646280(v=VS.85).aspx">WM_KEYDOWN</a>.


### -param lParam [in]

Specifies the repeat count, scan code, extended-key flag, context code, previous key-state flag, and transition-state flag of the key. For more information about this parameter, see the <i>lParam</i> parameter in <a href="https://msdn.microsoft.com/en-us/library/ms646280(v=VS.85).aspx">WM_KEYDOWN</a>.


### -param pfEaten [out]

Pointer to a BOOL that, on exit, indicates if the key event was handled. If this value receives <b>TRUE</b>, the key event was handled. If this value is <b>FALSE</b>, the key event was not handled.


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




<a href="https://msdn.microsoft.com/5fa1344f-d8c4-40d1-99df-3c493673ad87">ITfKeyEventSink</a>



<a href="https://msdn.microsoft.com/en-us/library/ms646280(v=VS.85).aspx">WM_KEYDOWN</a>
 

 

