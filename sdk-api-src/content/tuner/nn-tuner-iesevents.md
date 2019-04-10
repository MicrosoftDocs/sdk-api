---
UID: NN:tuner.IESEvents
title: IESEvents (tuner.h)
author: windows-sdk-content
description: Implements event handling for devices that have registered to receive specific events derived from the IESEvent interface. In a Protected Broadcast Driver Architecture graph, Media Sink Devices implement this interface to register for events.
old-location: mstv\iesevents.htm
tech.root: mstv
ms.assetid: 1921f632-bb3b-4833-aa25-9caa3d65363f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IESEvents, IESEvents interface [Microsoft TV Technologies], IESEvents interface [Microsoft TV Technologies],described, mstv.iesevents, tuner/IESEvents
ms.topic: interface
req.header: tuner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Tuner.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tuner.h
api_name:
 - IESEvents
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IESEvents interface


## -description


Implements event handling for devices that have registered to receive specific events derived from the <a href="https://msdn.microsoft.com/3c375480-c6df-4bb0-b417-5765b0bed9bf">IESEvent</a> interface. In a Protected Broadcast Driver Architecture graph, Media Sink Devices implement this interface to register for events.
      


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IESEvents</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IESEvents</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IESEvents</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d715f598-0dd5-4c8c-9f5b-3aaa65768600">OnESEventReceived</a>
</td>
<td align="left" width="63%">
Defines a handler for events derived from <a href="https://msdn.microsoft.com/3c375480-c6df-4bb0-b417-5765b0bed9bf">IESEvent</a>.
          

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IESEvents)</code>.



