---
UID: NN:subscriptionservices.IWMPSubscriptionService2
title: IWMPSubscriptionService2
author: windows-sdk-content
description: Note  This section describes functionality designed for use by online stores.
old-location: wmp\iwmpsubscriptionservice2.htm
tech.root: WMP
ms.assetid: 5338a3c1-c44a-4c03-a21a-6cd5cfeef064
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWMPSubscriptionService2, IWMPSubscriptionService2 interface [Windows Media Player], IWMPSubscriptionService2 interface [Windows Media Player],described, IWMPSubscriptionService2Interface, subscriptionservices/IWMPSubscriptionService2, wmp.iwmpsubscriptionservice2
ms.topic: interface
req.header: subscriptionservices.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - subscriptionservices.h
api_name:
 - IWMPSubscriptionService2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMPSubscriptionService2 interface


## -description



<div class="alert"><b>Note</b>  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported.</div>
<div> </div>
The <b>IWMPSubscriptionService2</b> interface extends <b>IWMPSubscriptionService</b>. It provides methods to initiate background processes, to provide notifications about online store activity, and to provide a pointer to the Windows Media Player core interface. These methods are implemented by the online store and called by Windows Media Player 10 or later.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMPSubscriptionService2</b> interface inherits from <a href="https://msdn.microsoft.com/en-us/library/Dd563697(v=VS.85).aspx">IWMPSubscriptionService</a>. <b>IWMPSubscriptionService2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMPSubscriptionService2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563699(v=VS.85).aspx">deviceAvailable</a>
</td>
<td align="left" width="63%">
Initiates device-specific processing tasks.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563700(v=VS.85).aspx">prepareForSync</a>
</td>
<td align="left" width="63%">
Initiates tasks related to synchronizing a digital media file to a device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563701(v=VS.85).aspx">serviceEvent</a>
</td>
<td align="left" width="63%">
Called when the online store is activated or deactivated.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563702(v=VS.85).aspx">stopBackgroundProcessing</a>
</td>
<td align="left" width="63%">
Terminates background processing tasks.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd563697(v=VS.85).aspx">IWMPSubscriptionService</a>



<a href="https://msdn.microsoft.com/b3f580cc-b02d-4312-a7a1-a35778a222bc">Reference for Type 2 Online Stores</a>
 

 

