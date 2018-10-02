---
UID: NF:d2d1.D2D1MakeSkewMatrix
title: D2D1MakeSkewMatrix function
author: windows-sdk-content
description: Creates a skew transformation that has the specified x-axis angle, y-axis angle, and center point.
old-location: direct2d\d2d1makeskewmatrix.htm
tech.root: direct2d
ms.assetid: 9f29488c-37f0-4d53-9e3b-3b27e841c8b4
ms.author: windowssdkdev
ms.date: 09/28/2018
ms.keywords: D2D1MakeSkewMatrix, D2D1MakeSkewMatrix function [Direct2D], d2d1/D2D1MakeSkewMatrix, direct2d.d2d1makeskewmatrix
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
 - D2D1MakeSkewMatrix
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# D2D1MakeSkewMatrix function


## -description


Creates a skew transformation that has the specified x-axis angle, y-axis angle, and center point. 


## -parameters




### -param angleX [in]

Type: <b>FLOAT</b>

The x-axis skew angle, which is measured in degrees counterclockwise from the y-axis.


### -param angleY [in]

Type: <b>FLOAT</b>

The y-axis skew angle, which is measured in degrees counterclockwise from the x-axis.


### -param center [in]

Type: <b><a href="https://msdn.microsoft.com/b317ae75-d738-4e1a-bcd1-adf3e95b197e">D2D1_POINT_2F</a></b>

The center point of the skew operation.


### -param matrix [out]

Type: <b><a href="https://msdn.microsoft.com/f05d7555-6482-4eea-950f-7b443892cc1f">D2D1_MATRIX_3X2_F</a>*</b>

When this method returns, contains the rotation transformation. You must allocate storate for this parameter.


## -returns



This function does not return a value.



