---
UID: NF:msctf.ITfKeystrokeMgr.AdviseKeyEventSink
title: ITfKeystrokeMgr::AdviseKeyEventSink
author: windows-sdk-content
description: ITfKeystrokeMgr::AdviseKeyEventSink method
old-location: tsf\itfkeystrokemgr_advisekeyeventsink.htm
old-project: TSF
ms.assetid: dfda786a-09f5-412c-878d-0ba0cbbdafe0
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: AdviseKeyEventSink, AdviseKeyEventSink method [Text Services Framework], AdviseKeyEventSink method [Text Services Framework],ITfKeystrokeMgr interface, ITfKeystrokeMgr interface [Text Services Framework],AdviseKeyEventSink method, ITfKeystrokeMgr.AdviseKeyEventSink, ITfKeystrokeMgr::AdviseKeyEventSink, _tsf_itfkeystrokemgr_advisekeyeventsink_ref, msctf/ITfKeystrokeMgr::AdviseKeyEventSink, tsf.itfkeystrokemgr_advisekeyeventsink
ms.prod: windows
ms.technology: windows-sdk
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
 - ITfKeystrokeMgr.AdviseKeyEventSink
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
req.product: GDI+ 1.1
---

# ITfKeystrokeMgr::AdviseKeyEventSink


## -description




## -parameters




### -param tid [in]

Identifier of the client that owns the key event sink. This value is obtained by a previous call to <a href="https://msdn.microsoft.com/bd9058c0-55b0-4231-a336-7cea4db75c0f">ITfThreadMgr::Activate</a>.


### -param pSink [in]

Pointer to a <a href="https://msdn.microsoft.com/5fa1344f-d8c4-40d1-99df-3c493673ad87">ITfKeyEventSink</a> interface.


### -param fForeground [in]

Specifies if this key event sink is made the foreground key event sink. If this is <b>TRUE</b>, this key event sink is made the foreground key event sink. Otherwise, this key event sink does not become the foreground key event sink.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more parameters are invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CONNECT_E_ADVISELIMIT</b></dt>
</dl>
</td>
<td width="60%">
The client identified by <i>tid</i> has a key event sink installed.

</td>
</tr>
</table>
 




## -remarks



The foreground key event sink receives all keyboard events. A non-foreground key event sink only receives preserved keys and key events that occur over text that marked owned by the client identifier.




## -see-also




<a href="https://msdn.microsoft.com/5fa1344f-d8c4-40d1-99df-3c493673ad87">ITfKeyEventSink
      </a>



<a href="https://msdn.microsoft.com/93c1591d-2c95-45cb-8fc5-5726e905f202">ITfKeystrokeMgr</a>



<a href="https://msdn.microsoft.com/bd9058c0-55b0-4231-a336-7cea4db75c0f">ITfThreadMgr::Activate
      </a>
 

 

