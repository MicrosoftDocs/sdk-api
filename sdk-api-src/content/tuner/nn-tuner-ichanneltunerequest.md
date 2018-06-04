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

# IChannelTuneRequest interface


## -description



        The <b>IChannelTuneRequest</b> interface is implemented on tuning request objects that support channel numbers, including analog TV and ATSC.

This interface enables a guide store loader running on Windows XP to create tuning requests for analog TV networks that an application can pass to the Video Control. The Video Control examines all tuning requests that it receives. If it is an analog tuning request, the Video Control creates a filter graph that can play the specified channel. Applications running on earlier versions of Windows are responsible for creating their own analog graphs if the user selects a program on an analog channel. Downlevel applications should not pass an analog tune request to a BDA tuning device because the device cannot interpret it.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IChannelTuneRequest</b> interface inherits from <a href="https://msdn.microsoft.com/34077b45-32b4-466b-b103-6a42fc869265">ITuneRequest</a>. <b>IChannelTuneRequest</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IChannelTuneRequest</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1a529416-9b7a-41f4-961a-741b1a581d5f">get_Channel</a>
</td>
<td align="left" width="63%">
Gets the channel to be tuned.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/67a08647-a2b5-43b2-b5d2-3917beb6dd27">put_Channel</a>
</td>
<td align="left" width="63%">
Sets the channel to be tuned.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IChannelTuneRequest)</code>.




## -see-also




<a href="https://msdn.microsoft.com/34077b45-32b4-466b-b103-6a42fc869265">ITuneRequest</a>



<a href="https://msdn.microsoft.com/5d956e1d-88b3-4236-9987-f37f674645de">Tuning Model Interfaces</a>
 

 

