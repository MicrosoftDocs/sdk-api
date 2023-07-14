---
UID: NF:tuner.IBDAComparable.HashExact
title: IBDAComparable::HashExact (tuner.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
helpviewer_keywords: ["HashExact","HashExact method [Microsoft TV Technologies]","HashExact method [Microsoft TV Technologies]","IBDAComparable interface","IBDAComparable interface [Microsoft TV Technologies]","HashExact method","IBDAComparable.HashExact","IBDAComparable::HashExact","IBDAComparableHashExact","mstv.ibdacomparable_hashexact","tuner/IBDAComparable::HashExact"]
old-location: mstv\ibdacomparable_hashexact.htm
tech.root: mstv
ms.assetid: 41495662-835b-47bc-a8d6-b0b689ec4d51
ms.date: 12/05/2018
ms.keywords: HashExact, HashExact method [Microsoft TV Technologies], HashExact method [Microsoft TV Technologies],IBDAComparable interface, IBDAComparable interface [Microsoft TV Technologies],HashExact method, IBDAComparable.HashExact, IBDAComparable::HashExact, IBDAComparableHashExact, mstv.ibdacomparable_hashexact, tuner/IBDAComparable::HashExact
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
 - IBDAComparable::HashExact
 - tuner/IBDAComparable::HashExact
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
 - IBDAComparable.HashExact
---

# IBDAComparable::HashExact


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>HashExact</b> method generates a hash code for all of the tuning properties of an object.

## -parameters

### -param Result [out]

Receives the result of the hash operation. This result is the hash code for the tuning properties of the object and its associated objects that are to be included in comparisons with other objects.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -remarks

This method generates a hash code from the values of the tuning properties in the object that implements the <b>IBDAComparable</b> interface, and its associated objects.

The caller can compare the resulting hash code to the hash code for another object of the same type to determine whether the two objects contain the same tuning information. The hash code incorporates the tuning properties in the object and its associated objects. If the hash codes for the two objects are identical, the two objects contain the same tuning information.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nf-tuner-ibdacomparable-hashexactincremental">HashExactIncremental</a>



<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ibdacomparable">IBDAComparable Interface</a>