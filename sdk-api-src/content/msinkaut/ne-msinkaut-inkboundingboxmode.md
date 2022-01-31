---
UID: NE:msinkaut.InkBoundingBoxMode
title: InkBoundingBoxMode (msinkaut.h)
description: Specifies which characteristics of a stroke, such as drawing attributes, are used to calculate the bounding box of the ink.The bounding box is the smallest rectangle that includes all points in the InkDisp object.
helpviewer_keywords: ["8c92fb43-1584-42fc-857e-aae5d5c222b4","IBBM_CurveFit","IBBM_Default","IBBM_NoCurveFit","IBBM_PointsOnly","IBBM_Union","InkBoundingBoxMode","InkBoundingBoxMode enumeration [Tablet PC]","msinkaut/IBBM_CurveFit","msinkaut/IBBM_Default","msinkaut/IBBM_NoCurveFit","msinkaut/IBBM_PointsOnly","msinkaut/IBBM_Union","msinkaut/InkBoundingBoxMode","tablet.inkboundingboxmode"]
old-location: tablet\inkboundingboxmode.htm
tech.root: tablet
ms.assetid: 8c92fb43-1584-42fc-857e-aae5d5c222b4
ms.date: 12/05/2018
ms.keywords: 8c92fb43-1584-42fc-857e-aae5d5c222b4, IBBM_CurveFit, IBBM_Default, IBBM_NoCurveFit, IBBM_PointsOnly, IBBM_Union, InkBoundingBoxMode, InkBoundingBoxMode enumeration [Tablet PC], msinkaut/IBBM_CurveFit, msinkaut/IBBM_Default, msinkaut/IBBM_NoCurveFit, msinkaut/IBBM_PointsOnly, msinkaut/IBBM_Union, msinkaut/InkBoundingBoxMode, tablet.inkboundingboxmode
req.header: msinkaut.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP Tablet PC Edition [desktop apps only]
req.target-min-winversvr: None supported
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
req.typenames: InkBoundingBoxMode
req.redist: 
ms.custom: 19H1
f1_keywords:
 - InkBoundingBoxMode
 - msinkaut/InkBoundingBoxMode
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - msinkaut.h
api_name:
 - InkBoundingBoxMode
---

# InkBoundingBoxMode enumeration


## -description

Specifies which characteristics of a stroke, such as drawing attributes, are used to calculate the bounding box of the ink.

The bounding box is the smallest rectangle that includes all points in the <a href="/windows/desktop/tablet/inkdisp-class">InkDisp</a> object. The size of the rectangle varies depending on whether you use drawing attributes, Bezier curve fitting, or just the points of the stroke to calculate the rectangle.

## -enum-fields

### -field IBBM_Default:0

 The definition of each stroke (polyline or Bezier) is used to calculate the bounding box; includes the drawing attributes, such as pen width, in the calculation.

### -field IBBM_NoCurveFit:1

 The polyline of the strokes (ignoring Bezier curve fitting requests) is used to calculate the bounding box; includes the drawing attributes in the calculation.

### -field IBBM_CurveFit:2

The  Bezier curve fitting line of the strokes (apply Bezier curve fitting to all strokes) is used to calculate the bounding box; includes the drawing attributes in the calculation.

### -field IBBM_PointsOnly:3

 Only the points of the strokes are used to calculate the bounding box.

### -field IBBM_Union:4

 The union of a NoCurveFit request and a CurveFit request.

## -see-also

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-getboundingbox">GetBoundingBox Method</a>



<a href="/windows/desktop/tablet/inkdisp-class">InkDisp Class</a>
