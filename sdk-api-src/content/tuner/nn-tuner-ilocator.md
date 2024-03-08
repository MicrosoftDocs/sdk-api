---
UID: NN:tuner.ILocator
title: ILocator (tuner.h)
description: The ILocator interface is implemented (through derived interfaces such as IATSCLocator) on Locator objects that contain tuning information about the tuning space.
helpviewer_keywords: ["ILocator","ILocator interface [Microsoft TV Technologies]","ILocator interface [Microsoft TV Technologies]","described","ILocatorInterface","mstv.ilocator","tuner/ILocator"]
old-location: mstv\ilocator.htm
tech.root: mstv
ms.assetid: 1d6c18f0-e7f1-4a1c-9edb-e4b66297becf
ms.date: 12/05/2018
ms.keywords: ILocator, ILocator interface [Microsoft TV Technologies], ILocator interface [Microsoft TV Technologies],described, ILocatorInterface, mstv.ilocator, tuner/ILocator
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
 - ILocator
 - tuner/ILocator
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
 - ILocator
---

# ILocator interface


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>ILocator</b> interface is implemented (through derived interfaces such as <a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-iatsclocator">IATSCLocator</a>) on Locator objects that contain tuning information about the tuning space. This base interface is never used directly, but only through the derived interfaces that are specific for a given network type.

 Locator objects can be created dynamically by Guide Store Loaders that have the necessary information about the tuning space, or a default locator for a tuning space can be installed by the third party who installs the tuning space. In any case, applications never create or examine locators except in certain testing or debugging scenarios. All Locator objects also support <b>IPersistPropertyBag</b>.

## -inheritance

The <b>ILocator</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ILocator</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(ILocator)</code>.

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="/previous-versions/windows/desktop/mstv/tuning-model-interfaces">Tuning Model Interfaces</a>
