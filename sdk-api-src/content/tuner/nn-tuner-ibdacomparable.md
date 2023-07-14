---
UID: NN:tuner.IBDAComparable
title: IBDAComparable (tuner.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
helpviewer_keywords: ["IBDAComparable","IBDAComparable interface [Microsoft TV Technologies]","IBDAComparable interface [Microsoft TV Technologies]","described","IBDAComparableInterface","mstv.ibdacomparable","tuner/IBDAComparable"]
old-location: mstv\ibdacomparable.htm
tech.root: mstv
ms.assetid: 6f582ae2-d8c6-4d85-a01f-e98c6ee16021
ms.date: 12/05/2018
ms.keywords: IBDAComparable, IBDAComparable interface [Microsoft TV Technologies], IBDAComparable interface [Microsoft TV Technologies],described, IBDAComparableInterface, mstv.ibdacomparable, tuner/IBDAComparable
req.header: tuner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - IBDAComparable
 - tuner/IBDAComparable
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
 - IBDAComparable
---

# IBDAComparable interface


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        

The <b>IBDAComparable</b> interface compares two objects to determine whether they contain the same or equivalent tuning information. DirectShow supports this interface in its implementation of the <a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-icomponent">IComponent</a>, <a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-icomponenttype">IComponentType</a>, <a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-itunerequest">ITuneRequest</a>, <a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ilocator">ILocator</a>, and <a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ituningspace">ITuningSpace</a> base interfaces and in the derived interfaces that inherit from these base interfaces. An application can query a component, component-type, tune-request, locator, or tuning-space object for an <b>IBDAComparable</b> interface that it can use to compare the tuning properties of the object to those of another object of the same type.

To support comparisons of the tuning properties of similar objects, two of the methods in this interface compare the property values directly. The remaining methods generate 64-bit CRC values from the property values for each object that the caller can compare to determine whether the objects have the same or equivalent properties.

## -inheritance

The <b>IBDAComparable</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IBDAComparable</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IBDAComparable)</code>.

## -see-also

<a href="/previous-versions/windows/desktop/mstv/bda-interfaces">BDA Interfaces</a>
