---
UID: NF:tuner.IATSCTuningSpace.put_MaxPhysicalChannel
title: IATSCTuningSpace::put_MaxPhysicalChannel (tuner.h)
description: The put_MaxPhysicalChannel method sets the highest physical channel number for this tuning space.
helpviewer_keywords: ["IATSCTuningSpace interface [Microsoft TV Technologies]","put_MaxPhysicalChannel method","IATSCTuningSpace.put_MaxPhysicalChannel","IATSCTuningSpace::put_MaxPhysicalChannel","IATSCTuningSpaceput_MaxPhysicalChannel","mstv.iatsctuningspace_put_maxphysicalchannel","put_MaxPhysicalChannel","put_MaxPhysicalChannel method [Microsoft TV Technologies]","put_MaxPhysicalChannel method [Microsoft TV Technologies]","IATSCTuningSpace interface","tuner/IATSCTuningSpace::put_MaxPhysicalChannel"]
old-location: mstv\iatsctuningspace_put_maxphysicalchannel.htm
tech.root: mstv
ms.assetid: 842d2c13-eef2-42d9-9642-50ec2aafb760
ms.date: 12/05/2018
ms.keywords: IATSCTuningSpace interface [Microsoft TV Technologies],put_MaxPhysicalChannel method, IATSCTuningSpace.put_MaxPhysicalChannel, IATSCTuningSpace::put_MaxPhysicalChannel, IATSCTuningSpaceput_MaxPhysicalChannel, mstv.iatsctuningspace_put_maxphysicalchannel, put_MaxPhysicalChannel, put_MaxPhysicalChannel method [Microsoft TV Technologies], put_MaxPhysicalChannel method [Microsoft TV Technologies],IATSCTuningSpace interface, tuner/IATSCTuningSpace::put_MaxPhysicalChannel
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
 - IATSCTuningSpace::put_MaxPhysicalChannel
 - tuner/IATSCTuningSpace::put_MaxPhysicalChannel
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
 - IATSCTuningSpace.put_MaxPhysicalChannel
---

# IATSCTuningSpace::put_MaxPhysicalChannel


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>put_MaxPhysicalChannel</b> method sets the highest physical channel number for this tuning space.

## -parameters

### -param NewMaxPhysicalChannelVal [in]

Variable of type <b>long</b> that specifies the highest physical channel.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-iatsctuningspace">IATSCTuningSpace Interface</a>



<a href="/previous-versions/windows/desktop/api/tuner/nf-tuner-ichanneltunerequest-put_channel">IChannelTuneRequest::put_Channel</a>