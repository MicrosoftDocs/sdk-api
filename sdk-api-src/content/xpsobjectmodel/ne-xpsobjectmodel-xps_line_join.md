---
UID: NE:xpsobjectmodel.__MIDL___MIDL_itf_xpsobjectmodel_0000_0000_0007
title: XPS_LINE_JOIN (xpsobjectmodel.h)
description: Describes the joint made by two intersecting line segments.
helpviewer_keywords: ["XPS_LINE_JOIN","XPS_LINE_JOIN enumeration [XPS Documents and Packaging]","XPS_LINE_JOIN_BEVEL","XPS_LINE_JOIN_MITER","XPS_LINE_JOIN_ROUND","xps.xps_line_join","xpsobjectmodel/XPS_LINE_JOIN","xpsobjectmodel/XPS_LINE_JOIN_BEVEL","xpsobjectmodel/XPS_LINE_JOIN_MITER","xpsobjectmodel/XPS_LINE_JOIN_ROUND"]
old-location: xps\xps_line_join.htm
tech.root: xps
ms.assetid: b0409564-a6b3-4e9d-b136-3d865dd46f1d
ms.date: 12/05/2018
ms.keywords: XPS_LINE_JOIN, XPS_LINE_JOIN enumeration [XPS Documents and Packaging], XPS_LINE_JOIN_BEVEL, XPS_LINE_JOIN_MITER, XPS_LINE_JOIN_ROUND, xps.xps_line_join, xpsobjectmodel/XPS_LINE_JOIN, xpsobjectmodel/XPS_LINE_JOIN_BEVEL, xpsobjectmodel/XPS_LINE_JOIN_MITER, xpsobjectmodel/XPS_LINE_JOIN_ROUND
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
req.typenames: XPS_LINE_JOIN
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_xpsobjectmodel_0000_0000_0007
 - xpsobjectmodel/__MIDL___MIDL_itf_xpsobjectmodel_0000_0000_0007
 - XPS_LINE_JOIN
 - xpsobjectmodel/XPS_LINE_JOIN
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
 - XPS_LINE_JOIN
---

# XPS_LINE_JOIN enumeration


## -description

Describes the joint made by two intersecting line segments.

## -enum-fields

### -field XPS_LINE_JOIN_MITER:1

Produces a sharp or clipped corner, depending on whether the length of the miter exceeds the miter limit.

### -field XPS_LINE_JOIN_BEVEL

Produces a diagonal corner.

### -field XPS_LINE_JOIN_ROUND

Produces a smooth, circular arc between the lines.

## -remarks

In the illustration that follows, the shaded area at the vertex of the line segments in each  example shows how the joint fill is determined by the value of <b>XPS_LINE_JOIN</b>.

<img alt="A diagram that shows examples of the different XPS_LINE_JOIN values" src="./images/XPS_LINE_JOIN.png"/>

## -see-also

<a href="https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf">XML Paper Specification</a>

