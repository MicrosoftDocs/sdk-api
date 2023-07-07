---
UID: NF:tuner.IATSCTuningSpace.get_MaxPhysicalChannel
title: IATSCTuningSpace::get_MaxPhysicalChannel (tuner.h)
description: The get_MaxPhysicalChannel method gets the highest physical channel number for this tuning space.
helpviewer_keywords: ["IATSCTuningSpace interface [Microsoft TV Technologies]","get_MaxPhysicalChannel method","IATSCTuningSpace.get_MaxPhysicalChannel","IATSCTuningSpace::get_MaxPhysicalChannel","IATSCTuningSpaceget_MaxPhysicalChannel","get_MaxPhysicalChannel","get_MaxPhysicalChannel method [Microsoft TV Technologies]","get_MaxPhysicalChannel method [Microsoft TV Technologies]","IATSCTuningSpace interface","mstv.iatsctuningspace_get_maxphysicalchannel","tuner/IATSCTuningSpace::get_MaxPhysicalChannel"]
old-location: mstv\iatsctuningspace_get_maxphysicalchannel.htm
tech.root: mstv
ms.assetid: 42aeab8d-f05c-423d-bd35-ac030adc6434
ms.date: 12/05/2018
ms.keywords: IATSCTuningSpace interface [Microsoft TV Technologies],get_MaxPhysicalChannel method, IATSCTuningSpace.get_MaxPhysicalChannel, IATSCTuningSpace::get_MaxPhysicalChannel, IATSCTuningSpaceget_MaxPhysicalChannel, get_MaxPhysicalChannel, get_MaxPhysicalChannel method [Microsoft TV Technologies], get_MaxPhysicalChannel method [Microsoft TV Technologies],IATSCTuningSpace interface, mstv.iatsctuningspace_get_maxphysicalchannel, tuner/IATSCTuningSpace::get_MaxPhysicalChannel
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
 - IATSCTuningSpace::get_MaxPhysicalChannel
 - tuner/IATSCTuningSpace::get_MaxPhysicalChannel
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
 - IATSCTuningSpace.get_MaxPhysicalChannel
---

# IATSCTuningSpace::get_MaxPhysicalChannel


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_MaxPhysicalChannel</b> method gets the highest physical channel number for this tuning space.

## -parameters

### -param MaxPhysicalChannelVal [out]

Receives the highest physical channel.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-iatsctuningspace">IATSCTuningSpace Interface</a>



<a href="/previous-versions/windows/desktop/api/tuner/nf-tuner-ichanneltunerequest-put_channel">IChannelTuneRequest::put_Channel</a>