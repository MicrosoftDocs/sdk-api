---
UID: NN:bdaiface.IBDA_NullTransform
title: IBDA_NullTransform (bdaiface.h)
description: The IBDA_NullTransform interface is implemented on all BDA device filters.
helpviewer_keywords: ["IBDA_NullTransform","IBDA_NullTransform interface [Microsoft TV Technologies]","IBDA_NullTransform interface [Microsoft TV Technologies]","described","IBDA_NullTransformInterface","bdaiface/IBDA_NullTransform","mstv.ibda_nulltransform"]
old-location: mstv\ibda_nulltransform.htm
tech.root: mstv
ms.assetid: f13350cb-5064-405d-aeb6-25f684d0bdbb
ms.date: 12/05/2018
ms.keywords: IBDA_NullTransform, IBDA_NullTransform interface [Microsoft TV Technologies], IBDA_NullTransform interface [Microsoft TV Technologies],described, IBDA_NullTransformInterface, bdaiface/IBDA_NullTransform, mstv.ibda_nulltransform
req.header: bdaiface.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - IBDA_NullTransform
 - bdaiface/IBDA_NullTransform
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - bdaiface.h
api_name:
 - IBDA_NullTransform
---

# IBDA_NullTransform interface


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>IBDA_NullTransform</b> interface is implemented on all BDA device filters. The Network Provider filter calls these methods to instruct the filter to either pass data through without modifying it, or else to perform its particular transformation on the data.

## -inheritance

The <b>IBDA_NullTransform</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IBDA_NullTransform</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IBDA_NullTransform)</code>.

## -see-also

<a href="/previous-versions/windows/desktop/mstv/bda-interfaces">BDA Interfaces</a>
