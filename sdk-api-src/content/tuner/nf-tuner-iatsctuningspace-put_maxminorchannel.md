---
UID: NF:tuner.IATSCTuningSpace.put_MaxMinorChannel
title: IATSCTuningSpace::put_MaxMinorChannel (tuner.h)
description: The put_MaxMinorChannel method gets the highest minor channel number for this tuning space.
helpviewer_keywords: ["IATSCTuningSpace interface [Microsoft TV Technologies]","put_MaxMinorChannel method","IATSCTuningSpace.put_MaxMinorChannel","IATSCTuningSpace::put_MaxMinorChannel","IATSCTuningSpaceput_MaxMinorChannel","mstv.iatsctuningspace_put_maxminorchannel","put_MaxMinorChannel","put_MaxMinorChannel method [Microsoft TV Technologies]","put_MaxMinorChannel method [Microsoft TV Technologies]","IATSCTuningSpace interface","tuner/IATSCTuningSpace::put_MaxMinorChannel"]
old-location: mstv\iatsctuningspace_put_maxminorchannel.htm
tech.root: mstv
ms.assetid: e90b78da-abd5-40bc-8d88-8a257acabe23
ms.date: 12/05/2018
ms.keywords: IATSCTuningSpace interface [Microsoft TV Technologies],put_MaxMinorChannel method, IATSCTuningSpace.put_MaxMinorChannel, IATSCTuningSpace::put_MaxMinorChannel, IATSCTuningSpaceput_MaxMinorChannel, mstv.iatsctuningspace_put_maxminorchannel, put_MaxMinorChannel, put_MaxMinorChannel method [Microsoft TV Technologies], put_MaxMinorChannel method [Microsoft TV Technologies],IATSCTuningSpace interface, tuner/IATSCTuningSpace::put_MaxMinorChannel
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
 - IATSCTuningSpace::put_MaxMinorChannel
 - tuner/IATSCTuningSpace::put_MaxMinorChannel
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
 - IATSCTuningSpace.put_MaxMinorChannel
---

# IATSCTuningSpace::put_MaxMinorChannel


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>put_MaxMinorChannel</b> method gets the highest minor channel number for this tuning space.

## -parameters

### -param NewMaxMinorChannelVal [in]

The highest minor channel.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -remarks

This property must be set before calling <a href="/previous-versions/windows/desktop/api/tuner/nf-tuner-iatsctuningspace-put_minminorchannel">put_MinMinorChannel</a> to avoid the case where the minimum minor channel is greater than the maximum minor channel. Both properties default to -1 (not set).

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-iatsctuningspace">IATSCTuningSpace Interface</a>