---
UID: NN:tuner.IATSCComponentType
title: IATSCComponentType (tuner.h)
description: The IATSCComponentType interface represents a component type for a component in an ATSC broadcast. The ATSCComponentType object exposes this interface. Use this interface to determine if an audio stream is in AC-3 format.
helpviewer_keywords: ["IATSCComponentType","IATSCComponentType interface [Microsoft TV Technologies]","IATSCComponentType interface [Microsoft TV Technologies]","described","IATSCComponentTypeInterface","mstv.iatsccomponenttype","tuner/IATSCComponentType"]
old-location: mstv\iatsccomponenttype.htm
tech.root: mstv
ms.assetid: c7e05f63-b2cf-4a99-8e0f-bc7ec00463cf
ms.date: 12/05/2018
ms.keywords: IATSCComponentType, IATSCComponentType interface [Microsoft TV Technologies], IATSCComponentType interface [Microsoft TV Technologies],described, IATSCComponentTypeInterface, mstv.iatsccomponenttype, tuner/IATSCComponentType
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
 - IATSCComponentType
 - tuner/IATSCComponentType
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
 - IATSCComponentType
---

# IATSCComponentType interface


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>IATSCComponentType</b> interface represents a component type for a component in an ATSC broadcast. The <a href="/previous-versions/windows/desktop/mstv/atsccomponenttype-object">ATSCComponentType</a> object exposes this interface. Use this interface to determine if an audio stream is in AC-3 format.

## -inheritance

The <b>IATSCComponentType</b> interface inherits from <a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-impeg2componenttype">IMPEG2ComponentType</a>. <b>IATSCComponentType</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IATSCComponentType)</code>.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-impeg2componenttype">IMPEG2ComponentType</a>



<a href="/previous-versions/windows/desktop/mstv/tuning-model-interfaces">Tuning Model Interfaces</a>
