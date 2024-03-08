---
UID: NF:tuner.IBDAComparable.CompareEquivalent
title: IBDAComparable::CompareEquivalent (tuner.h)
description: The CompareEquivalent method compares two objects to determine whether they contain equivalent tuning information.
helpviewer_keywords: ["CompareEquivalent","CompareEquivalent method [Microsoft TV Technologies]","CompareEquivalent method [Microsoft TV Technologies]","IBDAComparable interface","IBDAComparable interface [Microsoft TV Technologies]","CompareEquivalent method","IBDAComparable.CompareEquivalent","IBDAComparable::CompareEquivalent","IBDAComparableCompareEquivalent","mstv.ibdacomparable_compareequivalent","tuner/IBDAComparable::CompareEquivalent"]
old-location: mstv\ibdacomparable_compareequivalent.htm
tech.root: mstv
ms.assetid: 132c326e-053c-41be-b0fd-bea484fb0acd
ms.date: 12/05/2018
ms.keywords: CompareEquivalent, CompareEquivalent method [Microsoft TV Technologies], CompareEquivalent method [Microsoft TV Technologies],IBDAComparable interface, IBDAComparable interface [Microsoft TV Technologies],CompareEquivalent method, IBDAComparable.CompareEquivalent, IBDAComparable::CompareEquivalent, IBDAComparableCompareEquivalent, mstv.ibdacomparable_compareequivalent, tuner/IBDAComparable::CompareEquivalent
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
 - IBDAComparable::CompareEquivalent
 - tuner/IBDAComparable::CompareEquivalent
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
 - IBDAComparable.CompareEquivalent
---

# IBDAComparable::CompareEquivalent


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

<div class="alert"><b>Note</b>  This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.</div><div> </div>The <b>CompareEquivalent</b> method compares two objects to determine whether they contain equivalent tuning information.

## -parameters

### -param CompareTo [in]

Pointer to the <b>IDispatch</b> interface of the object that is to be compared with the object that implements the <a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ibdacomparable">IBDAComparable</a> interface.

### -param dwFlags [in]

Specifies whether to alter the default equivalence comparison. Setting this parameter to 0 invokes the default behavior. Setting this parameter to the bitwise OR of one or more <a href="/previous-versions/windows/desktop/mstv/bda-comp-flags">BDA_Comp_Flags</a> enumeration values overrides the default behavior.

### -param Result [out]

Receives the result of the comparison. If the result is 0, the two objects are equivalent. If the result is nonzero, the two objects are not equivalent.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -remarks

This method compares two objects to determine whether they have equivalent tuning properties. The first object in the comparison is the object that implements the <a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ibdacomparable">IBDAComparable</a> interface that the method is called on. The <i>CompareTo</i> parameter specifies the second object.

To determine whether the two objects contain equivalent tuning information, this method compares a subset of the tuning properties of the two objects and their associated objects. In contrast, the <a href="/previous-versions/windows/desktop/api/tuner/nf-tuner-ibdacomparable-compareexact">CompareExact</a> method compares all of these properties.

The tuning information is <i>equivalent</i> if the information in either object tunes to the same content. The implementation of the equivalence comparison depends on the object type.

For example, DirectShow implements the <b>IBDAComparable::CompareEquivalent</b> method for a tune-request object to include the tuning space in the default comparison but not to include the locator. Thus, two DVB tuning requests are equivalent if they both tune to the same DVB URL (with the same original network ID, transport stream ID, and service ID) regardless of whether they have the same modulation type.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ibdacomparable">IBDAComparable Interface</a>