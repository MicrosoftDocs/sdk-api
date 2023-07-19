---
UID: NF:tuner.IATSCTuningSpace.put_MinMinorChannel
title: IATSCTuningSpace::put_MinMinorChannel (tuner.h)
description: The put_MinMinorChannel method sets the lowest minor channel number ever allowed for this tuning space.
helpviewer_keywords: ["IATSCTuningSpace interface [Microsoft TV Technologies]","put_MinMinorChannel method","IATSCTuningSpace.put_MinMinorChannel","IATSCTuningSpace::put_MinMinorChannel","IATSCTuningSpaceput_MinMinorChannel","mstv.iatsctuningspace_put_minminorchannel","put_MinMinorChannel","put_MinMinorChannel method [Microsoft TV Technologies]","put_MinMinorChannel method [Microsoft TV Technologies]","IATSCTuningSpace interface","tuner/IATSCTuningSpace::put_MinMinorChannel"]
old-location: mstv\iatsctuningspace_put_minminorchannel.htm
tech.root: mstv
ms.assetid: 71ae8be2-8e80-49ff-9d1b-be42a620c20c
ms.date: 12/05/2018
ms.keywords: IATSCTuningSpace interface [Microsoft TV Technologies],put_MinMinorChannel method, IATSCTuningSpace.put_MinMinorChannel, IATSCTuningSpace::put_MinMinorChannel, IATSCTuningSpaceput_MinMinorChannel, mstv.iatsctuningspace_put_minminorchannel, put_MinMinorChannel, put_MinMinorChannel method [Microsoft TV Technologies], put_MinMinorChannel method [Microsoft TV Technologies],IATSCTuningSpace interface, tuner/IATSCTuningSpace::put_MinMinorChannel
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
 - IATSCTuningSpace::put_MinMinorChannel
 - tuner/IATSCTuningSpace::put_MinMinorChannel
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
 - IATSCTuningSpace.put_MinMinorChannel
---

# IATSCTuningSpace::put_MinMinorChannel


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>put_MinMinorChannel</b> method sets the lowest minor channel number ever allowed for this tuning space.

## -parameters

### -param NewMinMinorChannelVal [in]

Variable of type <b>long</b> that specifies the lowest minor channel.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -remarks

This property must be set after calling <a href="/previous-versions/windows/desktop/api/tuner/nf-tuner-iatsctuningspace-put_maxminorchannel">put_MaxMinorChannel</a> to avoid the case where the minimum minor channel is greater than the maximum minor channel. Both properties default to -1 (not set).

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-iatsctuningspace">IATSCTuningSpace Interface</a>