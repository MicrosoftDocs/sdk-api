---
UID: NN:eventsys.IPublisherFilter
title: IPublisherFilter
author: windows-sdk-content
description: Acts as a callback interface so that event publishers can control which subscribers receive event notifications or the order in which subscribers are notified.
old-location: cos\ipublisherfilter.htm
old-project: cossdk
ms.assetid: affc0af4-36f8-4479-8685-f91c29111d76
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: IPublisherFilter, IPublisherFilter interface [COM+], IPublisherFilter interface [COM+],described, _cos_IPublisherFilter, cos.ipublisherfilter, eventsys/IPublisherFilter
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: EOC_ChangeType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	EventSys.h
api_name:
-	IPublisherFilter
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IPublisherFilter interface


## -description


Acts as a callback interface so that event publishers can control which subscribers receive event notifications or the order in which subscribers are notified.


<b>IPublisherFilter</b> is supported only for backward compatibility. Instead, use the <a href="https://msdn.microsoft.com/f20f778b-fdd5-4c34-871b-d03cd1cd31cc">IMultiInterfacePublisherFilter</a> interface. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPublisherFilter</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IPublisherFilter</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IPublisherFilter</b> interface has these methods.
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
Associates an event method with a collection of subscription objects.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/78faa83f-ee73-4034-9be1-5576e5a909e3">PrepareToFire</a>
</td>
<td align="left" width="63%">
Prepares a publisher filter to begin firing a filtered list of subscriptions using a provided firing control.


</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/f20f778b-fdd5-4c34-871b-d03cd1cd31cc">IMultiInterfacePublisherFilter</a>
 

 

