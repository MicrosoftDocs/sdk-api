---
UID: NF:d2d1.D2D1InvertMatrix
title: D2D1InvertMatrix function
author: windows-sdk-content
description: Tries to invert the specified matrix.
old-location: direct2d\d2d1invertmatrix.htm
tech.root: Direct2D
ms.assetid: af01b6df-ada9-4e21-98f0-356b96d1017a
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: D2D1InvertMatrix, D2D1InvertMatrix function [Direct2D], d2d1/D2D1InvertMatrix, direct2d.d2d1invertmatrix
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
 - D2D1InvertMatrix
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# D2D1InvertMatrix function


## -description


Tries to invert the specified matrix.


## -parameters




### -param matrix [in, out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Dd368132(v=VS.85).aspx">D2D1_MATRIX_3X2_F</a>*</b>

The matrix to invert.


## -returns



Type: <b>BOOL</b>

<b>true</b> if the matrix was inverted; otherwise, <b>false</b>.



