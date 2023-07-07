---
UID: NN:tuner.IComponentTypes
title: IComponentTypes (tuner.h)
description: The IComponentTypes interface is implemented on ComponentTypes objects and contains methods that enable applications to enumerate, add, remove and retrieve individual ComponentType objects. All ComponentTypes objects also support IPersistPropertyBag.
helpviewer_keywords: ["IComponentTypes","IComponentTypes interface [Microsoft TV Technologies]","IComponentTypes interface [Microsoft TV Technologies]","described","IComponentTypesInterface","mstv.icomponenttypes","tuner/IComponentTypes"]
old-location: mstv\icomponenttypes.htm
tech.root: mstv
ms.assetid: 47c3837b-1348-4359-ad3d-3d82c5fe3781
ms.date: 12/05/2018
ms.keywords: IComponentTypes, IComponentTypes interface [Microsoft TV Technologies], IComponentTypes interface [Microsoft TV Technologies],described, IComponentTypesInterface, mstv.icomponenttypes, tuner/IComponentTypes
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
 - IComponentTypes
 - tuner/IComponentTypes
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
 - IComponentTypes
---

# IComponentTypes interface


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>IComponentTypes</b> interface is implemented on <a href="/previous-versions/windows/desktop/mstv/componenttypes-object">ComponentTypes</a> objects and contains methods that enable applications to enumerate, add, remove and retrieve individual <a href="/previous-versions/windows/desktop/legacy/dd693036(v=vs.85)">ComponentType</a> objects. All ComponentTypes objects also support <b>IPersistPropertyBag</b>.

## -inheritance

The <b>IComponentTypes</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IComponentTypes</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IComponentTypes)</code>.

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="/previous-versions/windows/desktop/mstv/tuning-model-interfaces">Tuning Model Interfaces</a>
