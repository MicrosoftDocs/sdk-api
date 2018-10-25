---
UID: NF:d2d1.D2D1MakeRotateMatrix
title: D2D1MakeRotateMatrix function
author: windows-sdk-content
description: Creates a rotation transformation that rotates by the specified angle about the specified point.
old-location: direct2d\d2d1makerotatematrix.htm
tech.root: direct2d
ms.assetid: 5e066328-5b0f-4e7a-9bf4-df55521fcc2b
ms.author: windowssdkdev
ms.date: 10/24/2018
ms.keywords: D2D1MakeRotateMatrix, D2D1MakeRotateMatrix function [Direct2D], d2d1/D2D1MakeRotateMatrix, direct2d.d2d1makerotatematrix
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
 - D2D1MakeRotateMatrix
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# D2D1MakeRotateMatrix function


## -description


Creates a rotation transformation that rotates by the specified angle about the specified point.


## -parameters




### -param angle [in]

Type: <b>FLOAT</b>

The clockwise rotation angle, in degrees. 


### -param center [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Dd368140(v=VS.85).aspx">D2D1_POINT_2F</a></b>

The point about which to rotate.


### -param matrix [out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Dd368132(v=VS.85).aspx">D2D1_MATRIX_3X2_F</a>*</b>

When this method returns, contains the new rotation transformation. You must allocate storage for this parameter.  


## -returns



This function does not return a value.




## -remarks



Rotation occurs in the plane of the 2-D surface.



