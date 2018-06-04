---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# ITfContextKeyEventSink interface


## -description


The <b>ITfContextKeyEventSink</b> interface is implemented by a text service to receive keyboard event notifications that occur in an input context. This keyboard event sink differs from the <a href="https://msdn.microsoft.com/5fa1344f-d8c4-40d1-99df-3c493673ad87">ITfKeyEventSink</a> keyboard event sink in that the keyboard events are passed to <b>ITfContextKeyEventSink</b> after having been preprocessed by the <b>ITfKeyEventSink</b> event sink. Preserved key events and filtered key events are not passed to the <b>ITfContextKeyEventSink</b> event sink.

This event sink is installed by <a href="https://msdn.microsoft.com/90928e6e-e11e-42ad-9b3e-d974642aca36">ITfSource::AdviseSink</a> with IID_ITfContextKeyEventSink.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfContextKeyEventSink</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITfContextKeyEventSink</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfContextKeyEventSink</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/684d3c01-fa95-4a19-b5fb-48a62315ce2f">OnKeyDown</a>
</td>
<td align="left" width="63%">
Called when a key down event occurs.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ed0c6e14-d216-425c-a194-08e8ea85bb92">OnKeyUp</a>
</td>
<td align="left" width="63%">
Called when a key up event occurs.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/26f22721-6d64-4637-92cd-8c18caa2d95f">OnTestKeyDown</a>
</td>
<td align="left" width="63%">
Called to determine if a text service will handle a key down event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0905b5e0-077e-4867-affa-9b2b542ec53d">OnTestKeyUp</a>
</td>
<td align="left" width="63%">
Called to determine if a text service will handle a key up event.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/ca98c7bb-7348-405d-976a-18012b0886c6">ITfContext
      </a>



<a href="https://msdn.microsoft.com/2ff77f09-1b4c-4115-9bb4-4040097d1f90">
        ITfSource
      </a>



<a href="https://msdn.microsoft.com/90928e6e-e11e-42ad-9b3e-d974642aca36">
        ITfSource::AdviseSink
      </a>



<a href="_COM_IUnknown">IUnknown</a>
 

 

