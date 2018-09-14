---
UID: NN:msctf.ITfKeystrokeMgr
title: ITfKeystrokeMgr
author: windows-sdk-content
description: The ITfKeystrokeMgr interface is implemented by the TSF manager and used by applications and text services to interact with the keyboard manager.
old-location: tsf\itfkeystrokemgr.htm
tech.root: TSF
ms.assetid: 93c1591d-2c95-45cb-8fc5-5726e905f202
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: ITfKeystrokeMgr, ITfKeystrokeMgr interface [Text Services Framework], ITfKeystrokeMgr interface [Text Services Framework],described, _tsf_itfkeystrokemgr_ref, msctf/ITfKeystrokeMgr, tsf.itfkeystrokemgr
ms.prod: windows
ms.technology: windows-sdk
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
 - ITfKeystrokeMgr
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# ITfKeystrokeMgr interface


## -description


The <b>ITfKeystrokeMgr</b> interface is implemented by the TSF manager and used by applications and text services to interact with the keyboard manager.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfKeystrokeMgr</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITfKeystrokeMgr</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfKeystrokeMgr</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dfda786a-09f5-412c-878d-0ba0cbbdafe0">AdviseKeyEventSink</a>
</td>
<td align="left" width="63%">
Installs a key event sink to receive keyboard events.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c447c4cb-47e3-4bc7-8eba-6e102762c69b">GetForeground</a>
</td>
<td align="left" width="63%">
Obtains the class identifier of the foreground TSF text service.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d87b3b1c-0e51-4e89-b837-79ed2fe78bbb">GetPreservedKey</a>
</td>
<td align="left" width="63%">
Obtains the command GUID for a preserved key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5ae2b56f-0dd9-4f37-a677-20b53c7200c7">GetPreservedKeyDescription</a>
</td>
<td align="left" width="63%">
Obtains the description string of an existing preserved key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/50deac9c-b659-494b-9cda-d6109fa39363">IsPreservedKey</a>
</td>
<td align="left" width="63%">
Determines if a command GUID and key combination is a preserved key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6eb4ad91-9431-4dec-b6cb-e58707318095">KeyDown</a>
</td>
<td align="left" width="63%">
Passes a key down event to the keystroke manager.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/14415de3-f397-4866-b7d1-167c0931a80c">KeyUp</a>
</td>
<td align="left" width="63%">
Passes a key up event to the keystroke manager.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ad5cd485-9231-4c29-8977-754dbf25c979">PreserveKey</a>
</td>
<td align="left" width="63%">
Registers a preserved key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/feb83f22-652c-4fec-b35d-a0cc41eab533">SetPreservedKeyDescription</a>
</td>
<td align="left" width="63%">
Modifies the description string of an existing preserved key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/09ad2203-a254-4afd-bdee-b8c51daa6e95">SimulatePreservedKey</a>
</td>
<td align="left" width="63%">
Simulates the execution of a preserved key sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e1f03aff-ce6e-4bb6-ad08-666e04cf6c13">TestKeyDown</a>
</td>
<td align="left" width="63%">
Determines if the keystroke manager will handle a key down event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/34a2b34b-3c3d-4609-a9e1-9b01ab349ae7">TestKeyUp</a>
</td>
<td align="left" width="63%">
Determines if the keystroke manager will handle a key up event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/72250972-0a0b-4e83-8603-0fb5adc9a2c9">UnadviseKeyEventSink</a>
</td>
<td align="left" width="63%">
Removes a key event sink.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/05975fce-04c3-4316-a9b2-ed015e7aa8fe">UnpreserveKey</a>
</td>
<td align="left" width="63%">
Unregisters a preserved key.

</td>
</tr>
</table> 

