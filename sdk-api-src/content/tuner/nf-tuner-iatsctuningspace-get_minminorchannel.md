---
UID: NF:tuner.IATSCTuningSpace.get_MinMinorChannel
title: IATSCTuningSpace::get_MinMinorChannel (tuner.h)
description: The get_MinMinorChannel method gets the lowest minor channel number ever allowed for this tuning space.
helpviewer_keywords: ["IATSCTuningSpace interface [Microsoft TV Technologies]","get_MinMinorChannel method","IATSCTuningSpace.get_MinMinorChannel","IATSCTuningSpace::get_MinMinorChannel","IATSCTuningSpaceget_MinMinorChannel","get_MinMinorChannel","get_MinMinorChannel method [Microsoft TV Technologies]","get_MinMinorChannel method [Microsoft TV Technologies]","IATSCTuningSpace interface","mstv.iatsctuningspace_get_minminorchannel","tuner/IATSCTuningSpace::get_MinMinorChannel"]
old-location: mstv\iatsctuningspace_get_minminorchannel.htm
tech.root: mstv
ms.assetid: 93068602-0efa-45f2-9883-d8b681cd3a0f
ms.date: 12/05/2018
ms.keywords: IATSCTuningSpace interface [Microsoft TV Technologies],get_MinMinorChannel method, IATSCTuningSpace.get_MinMinorChannel, IATSCTuningSpace::get_MinMinorChannel, IATSCTuningSpaceget_MinMinorChannel, get_MinMinorChannel, get_MinMinorChannel method [Microsoft TV Technologies], get_MinMinorChannel method [Microsoft TV Technologies],IATSCTuningSpace interface, mstv.iatsctuningspace_get_minminorchannel, tuner/IATSCTuningSpace::get_MinMinorChannel
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
 - IATSCTuningSpace::get_MinMinorChannel
 - tuner/IATSCTuningSpace::get_MinMinorChannel
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
 - IATSCTuningSpace.get_MinMinorChannel
---

# IATSCTuningSpace::get_MinMinorChannel


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_MinMinorChannel</b> method gets the lowest minor channel number ever allowed for this tuning space.

## -parameters

### -param MinMinorChannelVal [out]

Receives the lowest minor channel.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-iatsctuningspace">IATSCTuningSpace Interface</a>