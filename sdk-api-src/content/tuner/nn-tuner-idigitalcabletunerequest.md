---
UID: NN:tuner.IDigitalCableTuneRequest
title: IDigitalCableTuneRequest (tuner.h)
author: windows-sdk-content
description: The IDigitalCableTuneRequest interface provides methods for tuning to a channel in a digital cable network.
old-location: mstv\idigitalcabletunerequest.htm
tech.root: mstv
ms.assetid: 75c3c80f-2f02-4cb7-a9e0-aad4076793e4
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDigitalCableTuneRequest, IDigitalCableTuneRequest interface [Microsoft TV Technologies], IDigitalCableTuneRequest interface [Microsoft TV Technologies],described, IDigitalCableTuneRequestInterface, mstv.idigitalcabletunerequest, tuner/IDigitalCableTuneRequest
ms.topic: interface
req.header: tuner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
 - IDigitalCableTuneRequest
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDigitalCableTuneRequest interface


## -description



The <b>IDigitalCableTuneRequest</b> interface provides methods for tuning to a channel in a digital cable network. The <b>DigitalCableTuneRequest</b> object implements this interface.

<b>OCUR Devices: </b>This interface supports OpenCable Unidirectional Cable Receiver (OCUR) devices. See <a href="https://msdn.microsoft.com/7b641b94-9854-4ca8-8362-a9e1e49bbdd2">OCUR Devices</a>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDigitalCableTuneRequest</b> interface inherits from <a href="https://msdn.microsoft.com/9b55e181-ae03-473c-a85a-f169744d911d">IATSCChannelTuneRequest</a>. <b>IDigitalCableTuneRequest</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDigitalCableTuneRequest</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f8c59c66-1c86-4cfd-b295-ac1d1a75af17">get_MajorChannel</a>
</td>
<td align="left" width="63%">
Retrieves the major channel number.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3767a8b4-f318-4242-9b30-f1293b3f7091">get_SourceID</a>
</td>
<td align="left" width="63%">
Retrieves the source identifier, which maps to a physical channel.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1d3bc106-0ce0-4184-89fe-ebc30e95124e">put_MajorChannel</a>
</td>
<td align="left" width="63%">
Sets the major channel number.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4864f59c-5f06-419e-a0ca-d8bfb72a666c">put_SourceID</a>
</td>
<td align="left" width="63%">
Sets the source identifier.

</td>
</tr>
</table> 


## -remarks



This interface provides three ways to specify the program for the tune request:

<ul>
<li>Virtual channel number (VCN). To set the VCN, call <a href="https://msdn.microsoft.com/67a08647-a2b5-43b2-b5d2-3917beb6dd27">IChannelTuneRequest::put_Channel</a>. (This interface inherits <a href="https://msdn.microsoft.com/cdb65c1a-bd86-4dc8-a72f-c08e36999880">IChannelTuneRequest</a> through the <a href="https://msdn.microsoft.com/9b55e181-ae03-473c-a85a-f169744d911d">IATSCChannelTuneRequest</a> interface.)</li>
<li>Major channel and minor channel. These are used when an ATSC broadcast is transmitted over cable without remultiplexing the streams. To set the major and minor channels, call <a href="https://msdn.microsoft.com/1d3bc106-0ce0-4184-89fe-ebc30e95124e">IDigitalCableTuneRequest::put_MajorChannel</a> and <a href="https://msdn.microsoft.com/1288d249-58de-410e-852b-233133f56da5">IATSCChannelTuneRequest::put_MinorChannel</a>, respectively.</li>
<li>Source identifier. The source identifier is mapped to a physical channel in the virtual channel table. To set the source identifier, call <a href="https://msdn.microsoft.com/4864f59c-5f06-419e-a0ca-d8bfb72a666c">IDigitalCableTuneRequest::put_SourceID</a>.</li>
</ul>
Only one of these settings should be used in any one tune request. Set the other values equal to BDA_UNDEFINED_CHANNEL (-1). Also, if the physical channel is set in the locator, the physical channel overrides any of these values.

Note that the base channel number from <a href="https://msdn.microsoft.com/cdb65c1a-bd86-4dc8-a72f-c08e36999880">IChannelTuneRequest</a> has a different meaning when it is used in this interface than it does in the <a href="https://msdn.microsoft.com/9b55e181-ae03-473c-a85a-f169744d911d">IATSCChannelTuneRequest</a> interface. In this interface, the base channel number is the VCN, not the major channel.

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IDigitalCableTuneRequest)</code>.




## -see-also




<a href="https://msdn.microsoft.com/9b55e181-ae03-473c-a85a-f169744d911d">IATSCChannelTuneRequest</a>



<a href="https://msdn.microsoft.com/5d956e1d-88b3-4236-9987-f37f674645de">Tuning Model Interfaces</a>
 

 

