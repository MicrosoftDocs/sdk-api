---
UID: NN:tuner.IATSCLocator
title: IATSCLocator (tuner.h)
description: The IATSCLocator interface is implemented on the ATSCLocator object and contains methods that enable the network provider to determine the physical channel and transport stream ID of an ATSC transmission.
helpviewer_keywords: ["IATSCLocator","IATSCLocator interface [Microsoft TV Technologies]","IATSCLocator interface [Microsoft TV Technologies]","described","IATSCLocatorInterface","mstv.iatsclocator","tuner/IATSCLocator"]
old-location: mstv\iatsclocator.htm
tech.root: mstv
ms.assetid: 8ca7d50f-e7cc-4938-a2ed-fce5278b73fd
ms.date: 12/05/2018
ms.keywords: IATSCLocator, IATSCLocator interface [Microsoft TV Technologies], IATSCLocator interface [Microsoft TV Technologies],described, IATSCLocatorInterface, mstv.iatsclocator, tuner/IATSCLocator
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
 - IATSCLocator
 - tuner/IATSCLocator
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
 - IATSCLocator
---

# IATSCLocator interface


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>IATSCLocator</b> interface is implemented on the <a href="/previous-versions/windows/desktop/mstv/atsclocator-object">ATSCLocator</a> object and contains methods that enable the network provider to determine the physical channel and transport stream ID of an ATSC transmission. Applications do not use Locator interfaces except possibly for debugging purposes. All Locator objects also support <b>IPersistPropertyBag</b>.

## -inheritance

The <b>IATSCLocator</b> interface inherits from <a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-idigitallocator~r1">IDigitalLocator</a>. <b>IATSCLocator</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IATSCLocator)</code>.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-idigitallocator~r1">IDigitalLocator</a>



<a href="/previous-versions/windows/desktop/mstv/tuning-model-interfaces">Tuning Model Interfaces</a>
