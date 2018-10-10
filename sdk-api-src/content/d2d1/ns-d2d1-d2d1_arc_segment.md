---
UID: NS:d2d1.D2D1_ARC_SEGMENT
title: D2D1_ARC_SEGMENT
author: windows-sdk-content
description: Describes an elliptical arc between two points.
old-location: direct2d\D2D1_ARC_SEGMENT.htm
tech.root: Direct2D
ms.assetid: 3f391265-20b4-4897-aa0b-d14b71cd5f0a
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: D2D1_ARC_SEGMENT, D2D1_ARC_SEGMENT structure [Direct2D], d2d1/D2D1_ARC_SEGMENT, direct2d.D2D1_ARC_SEGMENT
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: d2d1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d2d1.h
api_name:
 - D2D1_ARC_SEGMENT
product: Windows
targetos: Windows
req.typenames: D2D1_ARC_SEGMENT
req.redist: 
---

# D2D1_ARC_SEGMENT structure


## -description


Describes an elliptical arc between two points.


## -struct-fields




### -field point

Type: <b><a href="https://msdn.microsoft.com/b317ae75-d738-4e1a-bcd1-adf3e95b197e">D2D1_POINT_2F</a></b>

The end point of the arc.


### -field size

Type: <b><a href="https://msdn.microsoft.com/c2fd41fb-72b3-418b-ad87-65549b04657d">D2D1_SIZE_F</a></b>

The x-radius and y-radius of the arc.


### -field rotationAngle

Type: <b>FLOAT</b>

A value that specifies how many degrees in the clockwise direction the ellipse is rotated relative to the current coordinate system.


### -field sweepDirection

Type: <b><a href="https://msdn.microsoft.com/97e6f384-7a42-4852-b948-66010bffed22">D2D1_SWEEP_DIRECTION</a></b>

A value that specifies whether the arc sweep is clockwise or counterclockwise.


### -field arcSize

Type: <b><a href="https://msdn.microsoft.com/c471716d-c2cc-4f79-8011-46690812b848">D2D1_ARC_SIZE</a></b>

A value that specifies whether the given arc is larger than 180 degrees.

