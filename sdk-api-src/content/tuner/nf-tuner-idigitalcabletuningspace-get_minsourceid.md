---
UID: NF:tuner.IDigitalCableTuningSpace.get_MinSourceID
title: IDigitalCableTuningSpace::get_MinSourceID (tuner.h)
description: The get_MinSourceID method retrieves the lowest source identifier for this tuning space.
helpviewer_keywords: ["IDigitalCableTuningSpace interface [Microsoft TV Technologies]","get_MinSourceID method","IDigitalCableTuningSpace.get_MinSourceID","IDigitalCableTuningSpace::get_MinSourceID","IDigitalCableTuningSpaceget_MinSourceID","get_MinSourceID","get_MinSourceID method [Microsoft TV Technologies]","get_MinSourceID method [Microsoft TV Technologies]","IDigitalCableTuningSpace interface","mstv.idigitalcabletuningspace_get_minsourceid","tuner/IDigitalCableTuningSpace::get_MinSourceID"]
old-location: mstv\idigitalcabletuningspace_get_minsourceid.htm
tech.root: mstv
ms.assetid: 54123d08-e01c-466e-833f-8412e06ac139
ms.date: 12/05/2018
ms.keywords: IDigitalCableTuningSpace interface [Microsoft TV Technologies],get_MinSourceID method, IDigitalCableTuningSpace.get_MinSourceID, IDigitalCableTuningSpace::get_MinSourceID, IDigitalCableTuningSpaceget_MinSourceID, get_MinSourceID, get_MinSourceID method [Microsoft TV Technologies], get_MinSourceID method [Microsoft TV Technologies],IDigitalCableTuningSpace interface, mstv.idigitalcabletuningspace_get_minsourceid, tuner/IDigitalCableTuningSpace::get_MinSourceID
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
 - IDigitalCableTuningSpace::get_MinSourceID
 - tuner/IDigitalCableTuningSpace::get_MinSourceID
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
 - IDigitalCableTuningSpace.get_MinSourceID
---

# IDigitalCableTuningSpace::get_MinSourceID


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_MinSourceID</b> method retrieves the lowest source identifier for this tuning space.

## -parameters

### -param MinSourceIDVal [out]

Receives the lowest source identifier.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-idigitalcabletuningspace">IDigitalCableTuningSpace Interface</a>