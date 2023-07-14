---
UID: NF:tuner.IATSCTuningSpace.get_MinPhysicalChannel
title: IATSCTuningSpace::get_MinPhysicalChannel (tuner.h)
description: The get_MinPhysicalChannel method sets the lowest physical channel number for this tuning space.
helpviewer_keywords: ["IATSCTuningSpace interface [Microsoft TV Technologies]","get_MinPhysicalChannel method","IATSCTuningSpace.get_MinPhysicalChannel","IATSCTuningSpace::get_MinPhysicalChannel","IATSCTuningSpaceget_MinPhysicalChannel","get_MinPhysicalChannel","get_MinPhysicalChannel method [Microsoft TV Technologies]","get_MinPhysicalChannel method [Microsoft TV Technologies]","IATSCTuningSpace interface","mstv.iatsctuningspace_get_minphysicalchannel","tuner/IATSCTuningSpace::get_MinPhysicalChannel"]
old-location: mstv\iatsctuningspace_get_minphysicalchannel.htm
tech.root: mstv
ms.assetid: 1b85331a-d99f-4cb6-8440-1b51fa697ade
ms.date: 12/05/2018
ms.keywords: IATSCTuningSpace interface [Microsoft TV Technologies],get_MinPhysicalChannel method, IATSCTuningSpace.get_MinPhysicalChannel, IATSCTuningSpace::get_MinPhysicalChannel, IATSCTuningSpaceget_MinPhysicalChannel, get_MinPhysicalChannel, get_MinPhysicalChannel method [Microsoft TV Technologies], get_MinPhysicalChannel method [Microsoft TV Technologies],IATSCTuningSpace interface, mstv.iatsctuningspace_get_minphysicalchannel, tuner/IATSCTuningSpace::get_MinPhysicalChannel
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IATSCTuningSpace::get_MinPhysicalChannel
 - tuner/IATSCTuningSpace::get_MinPhysicalChannel
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
 - IATSCTuningSpace.get_MinPhysicalChannel
---

# IATSCTuningSpace::get_MinPhysicalChannel


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_MinPhysicalChannel</b> method sets the lowest physical channel number for this tuning space.

## -parameters

### -param MinPhysicalChannelVal [out]

Receives the lowest physical channel.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-iatsctuningspace">IATSCTuningSpace Interface</a>



<a href="/previous-versions/windows/desktop/api/tuner/nf-tuner-ichanneltunerequest-put_channel">IChannelTuneRequest::put_Channel</a>