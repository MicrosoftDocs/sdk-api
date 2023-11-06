---
UID: NF:tuner.IDigitalCableTuningSpace.get_MinMajorChannel
title: IDigitalCableTuningSpace::get_MinMajorChannel (tuner.h)
description: The get_MinMajorChannel method retrieves the lowest major channel number for this tuning space.
helpviewer_keywords: ["IDigitalCableTuningSpace interface [Microsoft TV Technologies]","get_MinMajorChannel method","IDigitalCableTuningSpace.get_MinMajorChannel","IDigitalCableTuningSpace::get_MinMajorChannel","IDigitalCableTuningSpaceget_MinMajorChannel","get_MinMajorChannel","get_MinMajorChannel method [Microsoft TV Technologies]","get_MinMajorChannel method [Microsoft TV Technologies]","IDigitalCableTuningSpace interface","mstv.idigitalcabletuningspace_get_minmajorchannel","tuner/IDigitalCableTuningSpace::get_MinMajorChannel"]
old-location: mstv\idigitalcabletuningspace_get_minmajorchannel.htm
tech.root: mstv
ms.assetid: aa7df820-c970-4333-b4e3-54d68d951f1e
ms.date: 12/05/2018
ms.keywords: IDigitalCableTuningSpace interface [Microsoft TV Technologies],get_MinMajorChannel method, IDigitalCableTuningSpace.get_MinMajorChannel, IDigitalCableTuningSpace::get_MinMajorChannel, IDigitalCableTuningSpaceget_MinMajorChannel, get_MinMajorChannel, get_MinMajorChannel method [Microsoft TV Technologies], get_MinMajorChannel method [Microsoft TV Technologies],IDigitalCableTuningSpace interface, mstv.idigitalcabletuningspace_get_minmajorchannel, tuner/IDigitalCableTuningSpace::get_MinMajorChannel
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
 - IDigitalCableTuningSpace::get_MinMajorChannel
 - tuner/IDigitalCableTuningSpace::get_MinMajorChannel
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
 - IDigitalCableTuningSpace.get_MinMajorChannel
---

# IDigitalCableTuningSpace::get_MinMajorChannel


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_MinMajorChannel</b> method retrieves the lowest major channel number for this tuning space.

## -parameters

### -param MinMajorChannelVal [out]

Receives the lowest major channel number.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-idigitalcabletuningspace">IDigitalCableTuningSpace Interface</a>