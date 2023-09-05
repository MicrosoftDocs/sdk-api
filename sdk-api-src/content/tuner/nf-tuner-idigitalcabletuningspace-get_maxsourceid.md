---
UID: NF:tuner.IDigitalCableTuningSpace.get_MaxSourceID
title: IDigitalCableTuningSpace::get_MaxSourceID (tuner.h)
description: The get_MaxSourceID method retrieves the highest source identifier for this tuning space.
helpviewer_keywords: ["IDigitalCableTuningSpace interface [Microsoft TV Technologies]","get_MaxSourceID method","IDigitalCableTuningSpace.get_MaxSourceID","IDigitalCableTuningSpace::get_MaxSourceID","IDigitalCableTuningSpaceget_MaxSourceID","get_MaxSourceID","get_MaxSourceID method [Microsoft TV Technologies]","get_MaxSourceID method [Microsoft TV Technologies]","IDigitalCableTuningSpace interface","mstv.idigitalcabletuningspace_get_maxsourceid","tuner/IDigitalCableTuningSpace::get_MaxSourceID"]
old-location: mstv\idigitalcabletuningspace_get_maxsourceid.htm
tech.root: mstv
ms.assetid: 4f408777-11a0-4c86-95e6-9bfe7c917bb3
ms.date: 12/05/2018
ms.keywords: IDigitalCableTuningSpace interface [Microsoft TV Technologies],get_MaxSourceID method, IDigitalCableTuningSpace.get_MaxSourceID, IDigitalCableTuningSpace::get_MaxSourceID, IDigitalCableTuningSpaceget_MaxSourceID, get_MaxSourceID, get_MaxSourceID method [Microsoft TV Technologies], get_MaxSourceID method [Microsoft TV Technologies],IDigitalCableTuningSpace interface, mstv.idigitalcabletuningspace_get_maxsourceid, tuner/IDigitalCableTuningSpace::get_MaxSourceID
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
 - IDigitalCableTuningSpace::get_MaxSourceID
 - tuner/IDigitalCableTuningSpace::get_MaxSourceID
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
 - IDigitalCableTuningSpace.get_MaxSourceID
---

# IDigitalCableTuningSpace::get_MaxSourceID


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_MaxSourceID</b> method retrieves the highest source identifier for this tuning space.

## -parameters

### -param MaxSourceIDVal [out]

Receives the highest source identifier.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-idigitalcabletuningspace">IDigitalCableTuningSpace Interface</a>