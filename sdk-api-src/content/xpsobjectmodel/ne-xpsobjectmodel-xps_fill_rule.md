---
UID: NE:xpsobjectmodel.__MIDL___MIDL_itf_xpsobjectmodel_0000_0000_0010
title: XPS_FILL_RULE (xpsobjectmodel.h)
description: The rule used by a composite shape to determine whether a given point is part of the geometry.
helpviewer_keywords: ["XPS_FILL_RULE","XPS_FILL_RULE enumeration [XPS Documents and Packaging]","XPS_FILL_RULE_EVENODD","XPS_FILL_RULE_NONZERO","xps.xps_fill_rule","xpsobjectmodel/XPS_FILL_RULE","xpsobjectmodel/XPS_FILL_RULE_EVENODD","xpsobjectmodel/XPS_FILL_RULE_NONZERO"]
old-location: xps\xps_fill_rule.htm
tech.root: xps
ms.assetid: 353a4dc3-0c4d-46df-ae31-cc94c4116ca3
ms.date: 12/05/2018
ms.keywords: XPS_FILL_RULE, XPS_FILL_RULE enumeration [XPS Documents and Packaging], XPS_FILL_RULE_EVENODD, XPS_FILL_RULE_NONZERO, xps.xps_fill_rule, xpsobjectmodel/XPS_FILL_RULE, xpsobjectmodel/XPS_FILL_RULE_EVENODD, xpsobjectmodel/XPS_FILL_RULE_NONZERO
req.header: xpsobjectmodel.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: XpsObjectModel.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: XPS_FILL_RULE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_xpsobjectmodel_0000_0000_0010
 - xpsobjectmodel/__MIDL___MIDL_itf_xpsobjectmodel_0000_0000_0010
 - XPS_FILL_RULE
 - xpsobjectmodel/XPS_FILL_RULE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - xpsobjectmodel.h
api_name:
 - XPS_FILL_RULE
---

# XPS_FILL_RULE enumeration


## -description

The rule used by a composite shape to determine whether a given point is part of the geometry.

## -enum-fields

### -field XPS_FILL_RULE_EVENODD:1

The rule that determines whether a point is in the fill region. This is determined by drawing 
				a ray from the point to infinity in any direction, and counting the number 
				of path segments within the shape that the ray crosses. If this 
				number is odd, the point is inside; if even, the point is outside.

### -field XPS_FILL_RULE_NONZERO

The rule that determines whether a point is in the fill region of the 
				path. This is determined by drawing a ray from the point to infinity in any direction, and  
				examining the places where a segment of the shape crosses the ray. Start 
				the count at 0, then add 1 whenever a path segment crosses the ray from left 
				to right; subtract 1 whenever a path segment crosses the ray from 
				right to left. After the crossings are counted, 
				the point is outside the path if the result is zero and inside if otherwise.

## -see-also

<a href="https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf">XML Paper Specification</a>

