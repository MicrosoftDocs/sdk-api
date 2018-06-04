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

# ITuneRequest interface


## -description



The <b>ITuneRequest</b> interface is the base interface for all tune requests. Each tune request object supports a network-specific interface that derives from <b>ITuneRequest</b>, such as <a href="https://msdn.microsoft.com/9b55e181-ae03-473c-a85a-f169744d911d">IATSCChannelTuneRequest</a> or <a href="https://msdn.microsoft.com/4d519bbc-38e1-47ce-bd73-a3eb1ea399d6">IDVBTuneRequest</a>.

This interface is used by any application that creates tune requests, such as a Guide Store loader. A tune request must be associated with a specific network type. When a tune request is submitted, the derived interfaces are used by the Network Provider to extract the tuning information required by the hardware. All tune request objects also support <b>IPersistPropertyBag</b>, which enables them to be persisted in some type of third-party storage mechanism.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITuneRequest</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>ITuneRequest</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITuneRequest</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn938510">Clone</a>
</td>
<td align="left" width="63%">
Returns a new copy of this tune request.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f15ef4f6-ca36-4d46-93c7-26f1fbcb21cd">get_Components</a>
</td>
<td align="left" width="63%">
Retrieves the components contained in this tune request.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9f2a000a-0133-44f4-8e9c-7d37435596d7">get_Locator</a>
</td>
<td align="left" width="63%">
Called from the Network Provider to get the <a href="https://msdn.microsoft.com/1d6c18f0-e7f1-4a1c-9edb-e4b66297becf">ILocator</a> object associated with the requested broadcast.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6952df72-30f3-4c33-a0bf-d2ad8022042c">get_TuningSpace</a>
</td>
<td align="left" width="63%">
Retrieves the tuning space that was used to create this tune request.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/798ff904-5f08-4d3b-8a56-ca1c2df52aaf">put_Locator</a>
</td>
<td align="left" width="63%">
Called from the Network Provider to set the <a href="https://msdn.microsoft.com/1d6c18f0-e7f1-4a1c-9edb-e4b66297becf">ILocator</a> object associated with the requested broadcast.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(ITuneRequest)</code>.




## -see-also




<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>



<a href="https://msdn.microsoft.com/5d956e1d-88b3-4236-9987-f37f674645de">Tuning Model Interfaces</a>
 

 

