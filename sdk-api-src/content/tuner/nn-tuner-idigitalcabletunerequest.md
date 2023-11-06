---
UID: NN:tuner.IDigitalCableTuneRequest
title: IDigitalCableTuneRequest (tuner.h)
description: The IDigitalCableTuneRequest interface provides methods for tuning to a channel in a digital cable network.
helpviewer_keywords: ["IDigitalCableTuneRequest","IDigitalCableTuneRequest interface [Microsoft TV Technologies]","IDigitalCableTuneRequest interface [Microsoft TV Technologies]","described","IDigitalCableTuneRequestInterface","mstv.idigitalcabletunerequest","tuner/IDigitalCableTuneRequest"]
old-location: mstv\idigitalcabletunerequest.htm
tech.root: mstv
ms.assetid: 75c3c80f-2f02-4cb7-a9e0-aad4076793e4
ms.date: 12/05/2018
ms.keywords: IDigitalCableTuneRequest, IDigitalCableTuneRequest interface [Microsoft TV Technologies], IDigitalCableTuneRequest interface [Microsoft TV Technologies],described, IDigitalCableTuneRequestInterface, mstv.idigitalcabletunerequest, tuner/IDigitalCableTuneRequest
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDigitalCableTuneRequest
 - tuner/IDigitalCableTuneRequest
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tuner.h
api_name:
 - IDigitalCableTuneRequest
---

# IDigitalCableTuneRequest interface


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>IDigitalCableTuneRequest</b> interface provides methods for tuning to a channel in a digital cable network. The <b>DigitalCableTuneRequest</b> object implements this interface.

<b>OCUR Devices: </b>This interface supports OpenCable Unidirectional Cable Receiver (OCUR) devices. See <a href="/previous-versions/windows/desktop/mstv/ocur-devices">OCUR Devices</a>.

## -inheritance

The <b>IDigitalCableTuneRequest</b> interface inherits from <a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-iatscchanneltunerequest">IATSCChannelTuneRequest</a>. <b>IDigitalCableTuneRequest</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

This interface provides three ways to specify the program for the tune request:

<ul>
<li>Virtual channel number (VCN). To set the VCN, call <a href="/previous-versions/windows/desktop/api/tuner/nf-tuner-ichanneltunerequest-put_channel">IChannelTuneRequest::put_Channel</a>. (This interface inherits <a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ichanneltunerequest">IChannelTuneRequest</a> through the <a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-iatscchanneltunerequest">IATSCChannelTuneRequest</a> interface.)</li>
<li>Major channel and minor channel. These are used when an ATSC broadcast is transmitted over cable without remultiplexing the streams. To set the major and minor channels, call <a href="/previous-versions/windows/desktop/api/tuner/nf-tuner-idigitalcabletunerequest-put_majorchannel">IDigitalCableTuneRequest::put_MajorChannel</a> and <a href="/previous-versions/windows/desktop/api/tuner/nf-tuner-iatscchanneltunerequest-put_minorchannel">IATSCChannelTuneRequest::put_MinorChannel</a>, respectively.</li>
<li>Source identifier. The source identifier is mapped to a physical channel in the virtual channel table. To set the source identifier, call <a href="/previous-versions/windows/desktop/api/tuner/nf-tuner-idigitalcabletunerequest-put_sourceid">IDigitalCableTuneRequest::put_SourceID</a>.</li>
</ul>
Only one of these settings should be used in any one tune request. Set the other values equal to BDA_UNDEFINED_CHANNEL (-1). Also, if the physical channel is set in the locator, the physical channel overrides any of these values.

Note that the base channel number from <a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ichanneltunerequest">IChannelTuneRequest</a> has a different meaning when it is used in this interface than it does in the <a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-iatscchanneltunerequest">IATSCChannelTuneRequest</a> interface. In this interface, the base channel number is the VCN, not the major channel.

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IDigitalCableTuneRequest)</code>.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-iatscchanneltunerequest">IATSCChannelTuneRequest</a>



<a href="/previous-versions/windows/desktop/mstv/tuning-model-interfaces">Tuning Model Interfaces</a>
