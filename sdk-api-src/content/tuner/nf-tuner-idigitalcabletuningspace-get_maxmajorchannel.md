---
UID: NF:tuner.IDigitalCableTuningSpace.get_MaxMajorChannel
title: IDigitalCableTuningSpace::get_MaxMajorChannel (tuner.h)
description: The get_MaxMajorChannel method retrieves the highest major channel number for this tuning space.
helpviewer_keywords: ["IDigitalCableTuningSpace interface [Microsoft TV Technologies]","get_MaxMajorChannel method","IDigitalCableTuningSpace.get_MaxMajorChannel","IDigitalCableTuningSpace::get_MaxMajorChannel","IDigitalCableTuningSpaceget_MaxMajorChannel","get_MaxMajorChannel","get_MaxMajorChannel method [Microsoft TV Technologies]","get_MaxMajorChannel method [Microsoft TV Technologies]","IDigitalCableTuningSpace interface","mstv.idigitalcabletuningspace_get_maxmajorchannel","tuner/IDigitalCableTuningSpace::get_MaxMajorChannel"]
old-location: mstv\idigitalcabletuningspace_get_maxmajorchannel.htm
tech.root: mstv
ms.assetid: 00910dbb-3265-4e90-a5c5-110d7648e161
ms.date: 12/05/2018
ms.keywords: IDigitalCableTuningSpace interface [Microsoft TV Technologies],get_MaxMajorChannel method, IDigitalCableTuningSpace.get_MaxMajorChannel, IDigitalCableTuningSpace::get_MaxMajorChannel, IDigitalCableTuningSpaceget_MaxMajorChannel, get_MaxMajorChannel, get_MaxMajorChannel method [Microsoft TV Technologies], get_MaxMajorChannel method [Microsoft TV Technologies],IDigitalCableTuningSpace interface, mstv.idigitalcabletuningspace_get_maxmajorchannel, tuner/IDigitalCableTuningSpace::get_MaxMajorChannel
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
 - IDigitalCableTuningSpace::get_MaxMajorChannel
 - tuner/IDigitalCableTuningSpace::get_MaxMajorChannel
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
 - IDigitalCableTuningSpace.get_MaxMajorChannel
---

# IDigitalCableTuningSpace::get_MaxMajorChannel


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_MaxMajorChannel</b> method retrieves the highest major channel number for this tuning space.

## -parameters

### -param MaxMajorChannelVal [out]

Receives the highest major channel number.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-idigitalcabletuningspace">IDigitalCableTuningSpace Interface</a>