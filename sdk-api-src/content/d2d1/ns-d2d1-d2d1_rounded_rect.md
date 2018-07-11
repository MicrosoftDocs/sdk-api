---
UID: NS:d2d1.D2D1_ROUNDED_RECT
title: D2D1_ROUNDED_RECT
author: windows-sdk-content
description: Contains the dimensions and corner radii of a rounded rectangle.
old-location: direct2d\D2D1_ROUNDED_RECT.htm
old-project: direct2d
ms.assetid: 7069ca65-170e-42fc-8c1a-849a2f25c36f
ms.author: windowssdkdev
ms.date: 07/02/2018
ms.keywords: D2D1_ROUNDED_RECT, D2D1_ROUNDED_RECT structure [Direct2D], d2d1/D2D1_ROUNDED_RECT, direct2d.D2D1_ROUNDED_RECT
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: d2d1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: D2D1_ROUNDED_RECT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d2d1.h
api_name:
 - D2D1_ROUNDED_RECT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# D2D1_ROUNDED_RECT structure


## -description



    Contains the dimensions and corner radii of a rounded rectangle.


## -struct-fields




### -field rect

Type: <b><a href="https://msdn.microsoft.com/a961c0e3-fb76-4c07-b76e-47d8c09ada08">D2D1_RECT_F</a></b>

The coordinates of the rectangle.


### -field radiusX

Type: <b>FLOAT</b>

The x-radius for the quarter ellipse that is drawn to replace every corner of the rectangle.


### -field radiusY

Type: <b>FLOAT</b>

The y-radius for the quarter ellipse that is drawn to replace every corner of the rectangle.


## -remarks



Each corner of the rectangle specified by the <i>rect</i> is replaced with a quarter ellipse, with a radius in each direction specified by <i>radiusX</i> and <i>radiusY</i>.

 If the <i>radiusX</i> is greater than or equal to half the width of the rectangle, and the <i>radiusY</i> is greater than or equal to one-half the height, the rounded rectangle is an ellipse with the same width and height of the <i>rect</i>. 

Even when both <i>radiuX</i> and <i>radiusY</i> are zero, the rounded rectangle is different from a rectangle., When stroked, the corners of the rounded rectangle are roundly joined, not mitered (square). 



