---
UID: NN:tuner.IDigitalCableTuningSpace
title: IDigitalCableTuningSpace (tuner.h)
description: The IDigitalCableTuningSpace interface is implemented on the DigitalTuningSpace object and provides methods for working with tuning spaces that have a digital cable network type.
helpviewer_keywords: ["IDigitalCableTuningSpace","IDigitalCableTuningSpace interface [Microsoft TV Technologies]","IDigitalCableTuningSpace interface [Microsoft TV Technologies]","described","IDigitalCableTuningSpaceInterface","mstv.idigitalcabletuningspace","tuner/IDigitalCableTuningSpace"]
old-location: mstv\idigitalcabletuningspace.htm
tech.root: mstv
ms.assetid: a0788405-5502-4d6a-8f94-9957859ac1af
ms.date: 12/05/2018
ms.keywords: IDigitalCableTuningSpace, IDigitalCableTuningSpace interface [Microsoft TV Technologies], IDigitalCableTuningSpace interface [Microsoft TV Technologies],described, IDigitalCableTuningSpaceInterface, mstv.idigitalcabletuningspace, tuner/IDigitalCableTuningSpace
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
 - IDigitalCableTuningSpace
 - tuner/IDigitalCableTuningSpace
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
 - IDigitalCableTuningSpace
---

# IDigitalCableTuningSpace interface


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>IDigitalCableTuningSpace</b> interface is implemented on the DigitalTuningSpace object and provides methods for working with tuning spaces that have a digital cable network type.

## -inheritance

The <b>IDigitalCableTuningSpace</b> interface inherits from <a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-iatsctuningspace">IATSCTuningSpace</a>. <b>IDigitalCableTuningSpace</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

To set minimum and maximum values for the virtual channel number, use the <a href="/previous-versions/windows/desktop/api/tuner/nf-tuner-ianalogtvtuningspace-put_minchannel">IAnalogTVTuningSpace::put_MinChannel</a> and <a href="/previous-versions/windows/desktop/api/tuner/nf-tuner-ianalogtvtuningspace-put_maxchannel">IAnalogTVTuningSpace::put_MaxChannel</a> methods. (This interface inherits <a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ianalogtvtuningspace">IAnalogTVTuningSpace</a> through <a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-iatsctuningspace">IATSCTuningSpace</a>.)
      

To set minimum and maximum values for the minor channel number, use the <a href="/previous-versions/windows/desktop/api/tuner/nf-tuner-iatsctuningspace-put_minminorchannel">IATSCTuningSpace::put_MinMinorChannel</a> and <a href="/previous-versions/windows/desktop/api/tuner/nf-tuner-iatsctuningspace-put_maxminorchannel">IATSCTuningSpace::put_MaxMinorChannel</a> methods.
      

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IDigitalCableTuningSpace)</code>.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-iatsctuningspace">IATSCTuningSpace</a>



<a href="/previous-versions/windows/desktop/mstv/tuning-model-interfaces">Tuning Model Interfaces</a>
