---
UID: NF:tuner.IATSCTuningSpace.get_MaxMinorChannel
title: IATSCTuningSpace::get_MaxMinorChannel (tuner.h)
description: The get_MaxMinorChannel method gets the highest minor channel number for this tuning space.
helpviewer_keywords: ["IATSCTuningSpace interface [Microsoft TV Technologies]","get_MaxMinorChannel method","IATSCTuningSpace.get_MaxMinorChannel","IATSCTuningSpace::get_MaxMinorChannel","IATSCTuningSpaceget_MaxMinorChannel","get_MaxMinorChannel","get_MaxMinorChannel method [Microsoft TV Technologies]","get_MaxMinorChannel method [Microsoft TV Technologies]","IATSCTuningSpace interface","mstv.iatsctuningspace_get_maxminorchannel","tuner/IATSCTuningSpace::get_MaxMinorChannel"]
old-location: mstv\iatsctuningspace_get_maxminorchannel.htm
tech.root: mstv
ms.assetid: 55bfef31-f9c2-4edb-b4a9-369424584316
ms.date: 12/05/2018
ms.keywords: IATSCTuningSpace interface [Microsoft TV Technologies],get_MaxMinorChannel method, IATSCTuningSpace.get_MaxMinorChannel, IATSCTuningSpace::get_MaxMinorChannel, IATSCTuningSpaceget_MaxMinorChannel, get_MaxMinorChannel, get_MaxMinorChannel method [Microsoft TV Technologies], get_MaxMinorChannel method [Microsoft TV Technologies],IATSCTuningSpace interface, mstv.iatsctuningspace_get_maxminorchannel, tuner/IATSCTuningSpace::get_MaxMinorChannel
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
 - IATSCTuningSpace::get_MaxMinorChannel
 - tuner/IATSCTuningSpace::get_MaxMinorChannel
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
 - IATSCTuningSpace.get_MaxMinorChannel
---

# IATSCTuningSpace::get_MaxMinorChannel


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_MaxMinorChannel</b> method gets the highest minor channel number for this tuning space.

## -parameters

### -param MaxMinorChannelVal [out]

Receives the highest minor channel.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-iatsctuningspace">IATSCTuningSpace Interface</a>