---
UID: NN:tuner.IEnumComponentTypes
title: IEnumComponentTypes (tuner.h)
description: The IEnumComponentTypes interface is implemented on a standard COM collection of ComponentType objects associated with a given broadcast stream, and returned through a call to IComponentTypes::EnumComponentTypes.
helpviewer_keywords: ["IEnumComponentTypes","IEnumComponentTypes interface [Microsoft TV Technologies]","IEnumComponentTypes interface [Microsoft TV Technologies]","described","IEnumComponentTypesInterface","mstv.ienumcomponenttypes","tuner/IEnumComponentTypes"]
old-location: mstv\ienumcomponenttypes.htm
tech.root: mstv
ms.assetid: ad7fb66d-6592-47ae-9a2f-4432d8aaaebb
ms.date: 12/05/2018
ms.keywords: IEnumComponentTypes, IEnumComponentTypes interface [Microsoft TV Technologies], IEnumComponentTypes interface [Microsoft TV Technologies],described, IEnumComponentTypesInterface, mstv.ienumcomponenttypes, tuner/IEnumComponentTypes
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
 - IEnumComponentTypes
 - tuner/IEnumComponentTypes
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
 - IEnumComponentTypes
---

# IEnumComponentTypes interface


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>IEnumComponentTypes</b> interface is implemented on a standard COM collection of <a href="/previous-versions/windows/desktop/legacy/dd693036(v=vs.85)">ComponentType</a> objects associated with a given broadcast stream, and returned through a call to <a href="/previous-versions/windows/desktop/api/tuner/nf-tuner-icomponenttypes-enumcomponenttypes">IComponentTypes::EnumComponentTypes</a>.

## -inheritance

The <b>IEnumComponentTypes</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnumComponentTypes</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IEnumComponentTypes)</code>.

## -see-also

<a href="/previous-versions/windows/desktop/mstv/tuning-model-interfaces">Tuning Model Interfaces</a>
