---
UID: NN:tuner.IChannelTuneRequest
title: IChannelTuneRequest
author: windows-sdk-content
description: The IChannelTuneRequest interface is implemented on tuning request objects that support channel numbers, including analog TV and ATSC.
old-location: mstv\ichanneltunerequest.htm
tech.root: mstv
ms.assetid: cdb65c1a-bd86-4dc8-a72f-c08e36999880
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IChannelTuneRequest, IChannelTuneRequest interface [Microsoft TV Technologies], IChannelTuneRequest interface [Microsoft TV Technologies],described, IChannelTuneRequestInterface, mstv.ichanneltunerequest, tuner/IChannelTuneRequest
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: tuner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
 - IChannelTuneRequest
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
 

 

