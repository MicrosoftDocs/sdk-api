---
UID: NN:tuner.IESEventServiceConfiguration
title: IESEventServiceConfiguration
author: windows-driver-content
description: Contains methods that configure an event service that implements the IESEventService interface.
old-location: mstv\ieseventserviceconfiguration.htm
old-project: mstv
ms.assetid: 0b901732-42e1-4f50-904c-75d8202bb5b7
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: IESEventServiceConfiguration, IESEventServiceConfiguration interface [Microsoft TV Technologies], IESEventServiceConfiguration interface [Microsoft TV Technologies], described, mstv.ieseventserviceconfiguration, tuner/IESEventServiceConfiguration
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: BITMAP_RENDERER_STATISTICS, *PBITMAP_RENDERER_STATISTICS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	tuner.h
api_name:
-	IESEventServiceConfiguration
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IESEventServiceConfiguration interface


## -description



      Contains methods that configure an event service that implements the <a href="https://msdn.microsoft.com/2720d616-18a6-488e-98ef-565768c22c2a">IESEventService</a> interface. This interface allows you to create your own event service and set it up to receive events from a Protected Broadcast Driver Architecture (PBDA) event service, then pass those events to your event service's clients. 

For more information about PBDA, download the specification from <a href="http://go.microsoft.com/fwlink/p/?linkid=132926">http://go.microsoft.com/fwlink/p/?linkid=132926</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IESEventServiceConfiguration</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IESEventServiceConfiguration</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IESEventServiceConfiguration</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ba3d9748-5d3b-49ec-ac69-287a253caa12">RemoveGraph</a>
</td>
<td align="left" width="63%">

            Removes a PBDA event service from a filter  graph.
          

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c55b732e-960c-4a0c-939b-2f3628b5c9b6">RemoveOwner</a>
</td>
<td align="left" width="63%">

            Removes the owner of an <a href="https://msdn.microsoft.com/2720d616-18a6-488e-98ef-565768c22c2a">IESEventService</a> event service.
          

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/74d92e84-9819-49ed-bd56-26d6768f3ed0">RemoveParent</a>
</td>
<td align="left" width="63%">
Removes the parent of an <a href="https://msdn.microsoft.com/2720d616-18a6-488e-98ef-565768c22c2a">IESEventService</a> event service so that the event service can no longer pass events to the parent.
          

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0aee92b4-740a-4c5a-a64e-9de08d1c35c2">SetGraph</a>
</td>
<td align="left" width="63%">

            Attaches a PBDA event service to a filter  graph.
          

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7d8e1be1-b363-41ac-b60b-98415f0f44b6">SetOwner</a>
</td>
<td align="left" width="63%">
Specifies the <a href="https://msdn.microsoft.com/1921f632-bb3b-4833-aa25-9caa3d65363f">IESEvents</a> object that an <a href="https://msdn.microsoft.com/2720d616-18a6-488e-98ef-565768c22c2a">IESEventService</a> event service uses to pass advise events to its parent (the owner).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cfb931e9-f20f-4812-9d6b-cf8b651b7e7a">SetParent</a>
</td>
<td align="left" width="63%">
Specifies an event service (the parent) that another <a href="https://msdn.microsoft.com/2720d616-18a6-488e-98ef-565768c22c2a">IESEventService</a> event service can pass its events to.
          

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IESEventServiceConfiguration)</code>.




## -see-also




<a href="https://msdn.microsoft.com/2720d616-18a6-488e-98ef-565768c22c2a">IESEventService</a>



<a href="https://msdn.microsoft.com/1921f632-bb3b-4833-aa25-9caa3d65363f">IESEvents</a>
 

 

