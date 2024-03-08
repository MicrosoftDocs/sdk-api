---
UID: NN:tuner.IComponent
title: IComponent (tuner.h)
description: The IComponent interface a base class for all derived interfaces such as IMPEG2Component and it describes the general characteristics of a component, which is an elementary stream within the program stream.
helpviewer_keywords: ["IComponent","IComponent interface [Microsoft TV Technologies]","IComponent interface [Microsoft TV Technologies]","described","IComponentInterface","mstv.icomponent","tuner/IComponent"]
old-location: mstv\icomponent.htm
tech.root: mstv
ms.assetid: 516b30ba-4f55-49b7-8085-d436bf4a94e1
ms.date: 12/05/2018
ms.keywords: IComponent, IComponent interface [Microsoft TV Technologies], IComponent interface [Microsoft TV Technologies],described, IComponentInterface, mstv.icomponent, tuner/IComponent
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
 - IComponent
 - tuner/IComponent
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
 - IComponent
---

# IComponent interface


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>IComponent</b> interface a base class for all derived interfaces such as <a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-impeg2component">IMPEG2Component</a> and it describes the general characteristics of a component, which is an elementary stream within the program stream. The derived interfaces describe the properties of a component that are specific to a given network type. Component objects are created and attached to the tune request by the BDA Transport Information Filter (TIF) after reception has begun. All component objects also support <b>IPersistPropertyBag</b>.

## -inheritance

The <b>IComponent</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IComponent</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IComponent)</code>.

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="/previous-versions/windows/desktop/mstv/tuning-model-interfaces">Tuning Model Interfaces</a>
