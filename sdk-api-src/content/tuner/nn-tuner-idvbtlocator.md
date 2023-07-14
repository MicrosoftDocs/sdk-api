---
UID: NN:tuner.IDVBTLocator
title: IDVBTLocator (tuner.h)
description: The IDVBTLocator interface is implemented on the DVBTLocator object.
helpviewer_keywords: ["IDVBTLocator","IDVBTLocator interface [Microsoft TV Technologies]","IDVBTLocator interface [Microsoft TV Technologies]","described","IDVBTLocatorInterface","mstv.idvbtlocator","tuner/IDVBTLocator"]
old-location: mstv\idvbtlocator.htm
tech.root: mstv
ms.assetid: f5a95a68-fee0-404c-b9c6-6b808977f8d2
ms.date: 12/05/2018
ms.keywords: IDVBTLocator, IDVBTLocator interface [Microsoft TV Technologies], IDVBTLocator interface [Microsoft TV Technologies],described, IDVBTLocatorInterface, mstv.idvbtlocator, tuner/IDVBTLocator
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
 - IDVBTLocator
 - tuner/IDVBTLocator
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
 - IDVBTLocator
---

# IDVBTLocator interface


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>IDVBTLocator</b> interface is implemented on the <a href="/previous-versions/windows/desktop/mstv/dvbtlocator-object">DVBTLocator</a> object. It provides methods to enable a tuner to acquire a terrestrial DVB (DVB-T) transport stream. The data types are defined in Bdatypes.h. Locator data is meant for consumption by the BDA hardware drivers. Applications do not need to interpret any of this data except perhaps for some debugging purposes.

Locators can be created dynamically when the tune request is created, by a loader that has access to the necessary information about the tuning space, or a default locator can be installed when the tuning space is first installed, and the loader can use the default locator when creating tune requests. Applications do not need to use any of the Locator interfaces unless they are creating tune requests. All Locator objects also support <b>IPersistPropertyBag</b>.

## -inheritance

The <b>IDVBTLocator</b> interface inherits from <a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-idigitallocator~r1">IDigitalLocator</a>. <b>IDVBTLocator</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IDVBTLocator)</code>.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-idigitallocator~r1">IDigitalLocator</a>



<a href="/previous-versions/windows/desktop/mstv/tuning-model-interfaces">Tuning Model Interfaces</a>
