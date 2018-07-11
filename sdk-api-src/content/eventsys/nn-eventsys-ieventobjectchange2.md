---
UID: NN:eventsys.IEventObjectChange2
title: IEventObjectChange2
author: windows-sdk-content
description: Notifies subscribers of changes to the event store while including partition and application ID information.
old-location: cos\ieventobjectchange2.htm
old-project: cossdk
ms.assetid: 1b51c7ad-eae7-4030-81c2-ed9259648d31
ms.author: windowssdkdev
ms.date: 06/18/2018
ms.keywords: IEventObjectChange2, IEventObjectChange2 interface [COM+], IEventObjectChange2 interface [COM+],described, _cos_IEventObjectChange2, cos.ieventobjectchange2, eventsys/IEventObjectChange2
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
req.idl: Eventsys.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: EOC_ChangeType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Eventsys.h
api_name:
 - IEventObjectChange2
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IEventObjectChange2 interface


## -description


Notifies subscribers of changes to the event store while including partition and application ID information.

The <b>IEventObjectChange2</b> interface has the same firing characteristics as <a href="https://msdn.microsoft.com/2e916601-e03d-4c5f-a8fb-38317cfb66ad">IEventObjectChange</a>. 



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEventObjectChange2</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IEventObjectChange2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEventObjectChange2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ae760225-2c4f-46e5-8d35-eefec8f2f5da">ChangedEventClass</a>
</td>
<td align="left" width="63%">

Indicates that an event class object has been added, modified, or deleted.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/848d5af0-53aa-4ba4-9b21-0caf8e85d01d">ChangedSubscription</a>
</td>
<td align="left" width="63%">
Indicates that a subscription object has been added, modified, or deleted.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/2e916601-e03d-4c5f-a8fb-38317cfb66ad">IEventObjectChange</a>



<a href="https://msdn.microsoft.com/29b3e552-b717-4d10-9fa4-1386da3c5460">IEventSystem</a>
 

 

