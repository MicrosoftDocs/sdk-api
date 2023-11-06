---
UID: NN:tuner.IComponentType
title: IComponentType (tuner.h)
description: The IComponentType interface is implemented on ComponentType objects, and contains methods for setting and retrieving various properties for a Component.
helpviewer_keywords: ["IComponentType","IComponentType interface [Microsoft TV Technologies]","IComponentType interface [Microsoft TV Technologies]","described","IComponentTypeInterface","mstv.icomponenttype","tuner/IComponentType"]
old-location: mstv\icomponenttype.htm
tech.root: mstv
ms.assetid: e83bbbbe-64a9-4ed3-9c32-925ca80c2c38
ms.date: 12/05/2018
ms.keywords: IComponentType, IComponentType interface [Microsoft TV Technologies], IComponentType interface [Microsoft TV Technologies],described, IComponentTypeInterface, mstv.icomponenttype, tuner/IComponentType
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
 - IComponentType
 - tuner/IComponentType
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
 - IComponentType
---

# IComponentType interface


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>IComponentType</b> interface is implemented on <a href="/previous-versions/windows/desktop/legacy/dd693036(v=vs.85)">ComponentType</a> objects, and contains methods for setting and retrieving various properties for a Component. Every Component object has an associated ComponentType object that is set or retrieved with the <b>get_Type</b> and <b>put_Type</b> methods.

## -inheritance

The <b>IComponentType</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IComponentType</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IComponentType)</code>.

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="/previous-versions/windows/desktop/mstv/tuning-model-interfaces">Tuning Model Interfaces</a>
