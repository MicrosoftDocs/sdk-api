---
UID: NF:d2d1helper.StrokeStyleProperties
title: StrokeStyleProperties function
author: windows-sdk-content
description: Creates a D2D1_STROKE_STYLE_PROPERTIES structure.
old-location: direct2d\strokestyleproperties.htm
tech.root: Direct2D
ms.assetid: 7b7c2313-b105-45b2-9348-752ca44db716
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: StrokeStyleProperties, StrokeStyleProperties function [Direct2D], d2d1helper/StrokeStyleProperties, direct2d.strokestyleproperties
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: d2d1helper.h
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
req.lib: D2d1.lib
req.dll: D2d1.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - D2d1.dll
api_name:
 - StrokeStyleProperties
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# StrokeStyleProperties function


## -description


Creates a <a href="https://msdn.microsoft.com/en-us/library/Dd368164(v=VS.85).aspx">D2D1_STROKE_STYLE_PROPERTIES</a> structure. 


## -parameters




### -param startCap

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Dd368079(v=VS.85).aspx">D2D1_CAP_STYLE</a></b>

The shape at the beginning of a stroke. The default value is <a href="https://msdn.microsoft.com/en-us/library/Dd368079(v=VS.85).aspx">D2D1_CAP_STYLE_FLAT</a>.


### -param endCap

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Dd368079(v=VS.85).aspx">D2D1_CAP_STYLE</a></b>

The shape at the end of a stroke. The default value is <a href="https://msdn.microsoft.com/en-us/library/Dd368079(v=VS.85).aspx">D2D1_CAP_STYLE_FLAT</a>.


### -param dashCap

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Dd368079(v=VS.85).aspx">D2D1_CAP_STYLE</a></b>

The shape  at either end of each dash segment. The default value is <a href="https://msdn.microsoft.com/en-us/library/Dd368079(v=VS.85).aspx">D2D1_CAP_STYLE_FLAT</a>. 


### -param lineJoin

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Dd368130(v=VS.85).aspx">D2D1_LINE_JOIN</a></b>

A value that describes how segments are joined. The default value is <a href="https://msdn.microsoft.com/en-us/library/Dd368130(v=VS.85).aspx">D2D1_LINE_JOIN_MITER</a>.


### -param miterLimit

Type: <b>FLOAT</b>

The limit of the thickness of the join on a mitered corner. This value is always treated as though it is greater than or equal to 1.0f.

The default value is 10.0f.


### -param dashStyle

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Dd368087(v=VS.85).aspx">D2D1_DASH_STYLE</a></b>

A value that specifies whether the stroke has a dash pattern and, if so, the dash style. 

The default value is <a href="https://msdn.microsoft.com/en-us/library/Dd368087(v=VS.85).aspx">D2D1_DASH_STYLE_SOLID</a>.


### -param dashOffset

Type: <b>FLOAT</b>

A value that specifies how far in the dash sequence the stroke will start. 

The default value is 0.0f.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Dd368164(v=VS.85).aspx">D2D1_STROKE_STYLE_PROPERTIES</a></b>

The new stroke style.



