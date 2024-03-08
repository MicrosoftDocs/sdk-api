---
UID: NN:tuner.IATSCTuningSpace
title: IATSCTuningSpace (tuner.h)
description: The IATSCTuningSpace interface is implemented on ATSCTuningSpace objects, which represent any tuning space with an ATSC network type.
helpviewer_keywords: ["IATSCTuningSpace","IATSCTuningSpace interface [Microsoft TV Technologies]","IATSCTuningSpace interface [Microsoft TV Technologies]","described","IATSCTuningSpaceInterface","mstv.iatsctuningspace","tuner/IATSCTuningSpace"]
old-location: mstv\iatsctuningspace.htm
tech.root: mstv
ms.assetid: 313508e5-a9b2-42b8-bb2f-d191944d0939
ms.date: 12/05/2018
ms.keywords: IATSCTuningSpace, IATSCTuningSpace interface [Microsoft TV Technologies], IATSCTuningSpace interface [Microsoft TV Technologies],described, IATSCTuningSpaceInterface, mstv.iatsctuningspace, tuner/IATSCTuningSpace
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
 - IATSCTuningSpace
 - tuner/IATSCTuningSpace
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
 - IATSCTuningSpace
---

# IATSCTuningSpace interface


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>IATSCTuningSpace</b> interface is implemented on <a href="/previous-versions/windows/desktop/mstv/atsctuningspace-object">ATSCTuningSpace</a> objects, which represent any tuning space with an ATSC network type. Microsoft provides a default ATSC tuning space with Windows XP, and also with DirectX 9.0. Third parties such as cable providers may install a custom tuning space using the <a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ituningspacecontainer">ITuningSpaceContainer</a> interface. An ATSCTuningSpace object creates tune requests that expose <a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-iatscchanneltunerequest">IATSCChannelTuneRequest</a>.

## -inheritance

The <b>IATSCTuningSpace</b> interface inherits from <a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ianalogtvtuningspace">IAnalogTVTuningSpace</a>. <b>IATSCTuningSpace</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

If the minimum and maximum channels are set, and the user specifies a channel that is greater than the maximum, the tuner automatically wraps around to the minimum value.

To set the minimum and maximum major channel, call <a href="/previous-versions/windows/desktop/api/tuner/nf-tuner-ianalogtvtuningspace-put_minchannel">IAnalogTVTuningSpace::put_MinChannel</a> and <a href="/previous-versions/windows/desktop/api/tuner/nf-tuner-ianalogtvtuningspace-put_maxchannel">IAnalogTVTuningSpace::put_MaxChannel</a>.

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IATSCTuningSpace)</code>.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ianalogtvtuningspace">IAnalogTVTuningSpace</a>



<a href="/previous-versions/windows/desktop/mstv/tuning-model-interfaces">Tuning Model Interfaces</a>
