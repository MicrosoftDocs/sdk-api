---
UID: NN:msctf.ITfKeyEventSink
title: ITfKeyEventSink
author: windows-sdk-content
description: The ITfKeyEventSink interface is implemented by a text service to receive keyboard and focus event notifications. To install this event sink, call ITfKeystrokeMgr::AdviseKeyEventSink.
old-location: tsf\itfkeyeventsink.htm
tech.root: TSF
ms.assetid: 5fa1344f-d8c4-40d1-99df-3c493673ad87
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: ITfKeyEventSink, ITfKeyEventSink interface [Text Services Framework], ITfKeyEventSink interface [Text Services Framework],described, _tsf_itfkeyeventsink_ref, msctf/ITfKeyEventSink, tsf.itfkeyeventsink
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
 - msctf.dll
api_name:
 - ITfKeyEventSink
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# ITfKeyEventSink interface


## -description


The <b>ITfKeyEventSink</b> interface is implemented by a text service to receive keyboard and focus event notifications. To install this event sink, call <a href="https://msdn.microsoft.com/dfda786a-09f5-412c-878d-0ba0cbbdafe0">ITfKeystrokeMgr::AdviseKeyEventSink</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfKeyEventSink</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITfKeyEventSink</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfKeyEventSink</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/aceeb367-0963-484b-afae-26a2c4fb24c7">OnKeyDown</a>
</td>
<td align="left" width="63%">
Called when a key down event occurs.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5718a15b-985e-4286-a963-cee513e7550c">OnKeyUp</a>
</td>
<td align="left" width="63%">
Called when a key up event occurs.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/90b3f2f4-5655-42e3-bdef-62c090800e5e">OnPreservedKey</a>
</td>
<td align="left" width="63%">
Called when a preserved key event occurs.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/999c7ead-7ca6-42a5-a530-706fb3283b21">OnSetFocus</a>
</td>
<td align="left" width="63%">
Called when a TSF text service receives or loses the keyboard focus.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3d8056ef-c012-4989-91ce-65ae8cd39404">OnTestKeyDown</a>
</td>
<td align="left" width="63%">
Called to determine if a text service will handle a key down event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2d105a20-3fb8-43aa-a36a-744803bd4035">OnTestKeyUp</a>
</td>
<td align="left" width="63%">
Called to determine if a text service will handle a key up event.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/dfda786a-09f5-412c-878d-0ba0cbbdafe0">ITfKeystrokeMgr::AdviseKeyEventSink
      </a>



<a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a>
 

 

