---
UID: NN:eventsys.IMultiInterfacePublisherFilter
title: IMultiInterfacePublisherFilter
author: windows-driver-content
description: Manages a filtered subscription cache for an event method.
old-location: cos\imultiinterfacepublisherfilter.htm
old-project: cossdk
ms.assetid: f20f778b-fdd5-4c34-871b-d03cd1cd31cc
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: IMultiInterfacePublisherFilter, IMultiInterfacePublisherFilter interface [COM+], IMultiInterfacePublisherFilter interface [COM+],described, _cos_IMultiInterfacePublisherFilter, cos.imultiinterfacepublisherfilter, eventsys/IMultiInterfacePublisherFilter
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: eventsys.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: EventSys.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: EOC_ChangeType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	EventSys.h
api_name:
-	IMultiInterfacePublisherFilter
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IMultiInterfacePublisherFilter interface


## -description


Manages a filtered subscription cache for an event method. Only subscribers who meet the criteria specified by the filter are notified when the associated event is fired. The <b>IMultiInterfacePublisherFilter</b> interface differs from the <a href="https://msdn.microsoft.com/affc0af4-36f8-4479-8685-f91c29111d76">IPublisherFilter</a> interface in that it supports multiple event interfaces for the event object.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMultiInterfacePublisherFilter</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMultiInterfacePublisherFilter</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMultiInterfacePublisherFilter</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff550945">Initialize</a>
</td>
<td align="left" width="63%">

Associates an event class with a publisher filter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a9257017-a9e7-4a0a-9dee-55493a659bda">PrepareToFire</a>
</td>
<td align="left" width="63%">

Prepares the publisher filter to begin firing a filtered list of subscriptions using a provided firing control. The firing control is contained in the event class object.

</td>
</tr>
</table> 

