---
UID: NN:tuner.IATSCChannelTuneRequest
title: IATSCChannelTuneRequest
author: windows-sdk-content
description: The IATSCChannelTuneRequest interface provides methods for tuning to a channel in an ATSC network. The ATSCChannelTuneRequest object implements this interface.
old-location: mstv\iatscchanneltunerequest.htm
tech.root: MSTV
ms.assetid: 9b55e181-ae03-473c-a85a-f169744d911d
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IATSCChannelTuneRequest, IATSCChannelTuneRequest interface [Microsoft TV Technologies], IATSCChannelTuneRequest interface [Microsoft TV Technologies],described, IATSCChannelTuneRequestInterface, mstv.iatscchanneltunerequest, tuner/IATSCChannelTuneRequest
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
 - IATSCChannelTuneRequest
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IATSCChannelTuneRequest interface


## -description



The <b>IATSCChannelTuneRequest</b> interface provides methods for tuning to a channel in an ATSC network. The <a href="https://msdn.microsoft.com/5b252438-88c4-4b61-a64b-f5fbbac45a06">ATSCChannelTuneRequest</a> object implements this interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IATSCChannelTuneRequest</b> interface inherits from <a href="https://msdn.microsoft.com/cdb65c1a-bd86-4dc8-a72f-c08e36999880">IChannelTuneRequest</a>. <b>IATSCChannelTuneRequest</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IATSCChannelTuneRequest</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2b8aa006-faba-472b-836b-0ff1ae134232">get_MinorChannel</a>
</td>
<td align="left" width="63%">
Gets the current minor channel.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1288d249-58de-410e-852b-233133f56da5">put_MinorChannel</a>
</td>
<td align="left" width="63%">
Sets the minor channel to be tuned.

</td>
</tr>
</table> 


## -remarks



ATSC defines a tune request in terms of a <i>major channel</i> and a <i>minor channel</i>. The major channel is mapped to a physical frequency and the minor channel identifies different programs within the same major channel. To access the channel numbers, use the following methods:

<ul>
<li>Major channel: <ul>
<li>
<a href="https://msdn.microsoft.com/1a529416-9b7a-41f4-961a-741b1a581d5f">IChannelTuneRequest::get_Channel</a>
</li>
<li>
<a href="https://msdn.microsoft.com/67a08647-a2b5-43b2-b5d2-3917beb6dd27">IChannelTuneRequest::put_Channel</a>
</li>
</ul>
</li>
<li>Minor channel: <ul>
<li>
<a href="https://msdn.microsoft.com/2b8aa006-faba-472b-836b-0ff1ae134232">IATSCChannelTuneRequest::get_MinorChannel</a>
</li>
<li>
<a href="https://msdn.microsoft.com/1288d249-58de-410e-852b-233133f56da5">IATSCChannelTuneRequest::put_MinorChannel</a>
</li>
</ul>
</li>
</ul>
To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IATSCChannelTuneRequest)</code>.




## -see-also




<a href="https://msdn.microsoft.com/cdb65c1a-bd86-4dc8-a72f-c08e36999880">IChannelTuneRequest</a>



<a href="https://msdn.microsoft.com/5d956e1d-88b3-4236-9987-f37f674645de">Tuning Model Interfaces</a>
 

 

