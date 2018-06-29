---
UID: NF:msctf.ITfKeyEventSink.OnKeyUp
title: ITfKeyEventSink::OnKeyUp
author: windows-sdk-content
description: ITfKeyEventSink::OnKeyUp method
old-location: tsf\itfkeyeventsink_onkeyup.htm
old-project: TSF
ms.assetid: 5718a15b-985e-4286-a963-cee513e7550c
ms.author: windowssdkdev
ms.date: 06/01/2018
ms.keywords: ITfKeyEventSink interface [Text Services Framework],OnKeyUp method, ITfKeyEventSink.OnKeyUp, ITfKeyEventSink::OnKeyUp, OnKeyUp, OnKeyUp method [Text Services Framework], OnKeyUp method [Text Services Framework],ITfKeyEventSink interface, _tsf_itfkeyeventsink_onkeyup_ref, msctf/ITfKeyEventSink::OnKeyUp, tsf.itfkeyeventsink_onkeyup
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps | UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: TF_DA_ATTR_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msctf.dll
api_name:
 - ITfKeyEventSink.OnKeyUp
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
req.product: GDI+ 1.1
---

# ITfKeyEventSink::OnKeyUp


## -description




## -parameters




### -param pic [in]

Pointer to the input context that receives the key event.


### -param wParam [in]

Specifies the virtual-key code of the key. For more information about this parameter, see the <i>wParam</i> parameter in <a href="https://msdn.microsoft.com/library/ms646281(v=VS.85).aspx">WM_KEYUP</a>.


### -param lParam [in]

Specifies the repeat count, scan code, extended-key flag, context code, previous key-state flag, and transition-state flag of the key. For more information about this parameter, see the <i>lParam</i> parameter in <a href="https://msdn.microsoft.com/library/ms646281(v=VS.85).aspx">WM_KEYUP</a>.


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
 



