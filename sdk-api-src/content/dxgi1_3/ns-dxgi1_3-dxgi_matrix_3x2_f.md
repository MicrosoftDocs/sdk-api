---
UID: NS:dxgi1_3.DXGI_MATRIX_3X2_F
title: DXGI_MATRIX_3X2_F
author: windows-sdk-content
description: Represents a 3x2 matrix. Used with GetMatrixTransform and SetMatrixTransform to indicate the scaling and translation transform for SwapChainPanel swap chains.
old-location: direct3ddxgi\dxgi_matrix_3x2_f.htm
old-project: direct3ddxgi
ms.assetid: 5EA0FAD4-5F19-4E5A-97D4-11AE750E8560
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: DXGI_MATRIX_3X2_F, DXGI_MATRIX_3X2_F structure [DXGI], direct3ddxgi.dxgi_matrix_3x2_f, dxgi1_3/DXGI_MATRIX_3X2_F
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: dxgi1_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps \| UWP apps]
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
req.typenames: DXGI_MATRIX_3X2_F
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dxgi1_3.h
api_name:
 - DXGI_MATRIX_3X2_F
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# DXGI_MATRIX_3X2_F structure


## -description


Represents a 3x2 matrix. Used with <a href="https://msdn.microsoft.com/90302283-BB0A-44A9-8CD2-591571EF74ED">GetMatrixTransform</a> and <a href="https://msdn.microsoft.com/AAED8A59-3190-49A0-93AA-F5CAF9088877">SetMatrixTransform</a> to indicate the scaling and translation transform for <a href="https://msdn.microsoft.com/e99a6d0f-d556-4aaa-853a-366853614560">SwapChainPanel</a> swap chains.


## -struct-fields




### -field _11

The value in the first row and first column of the matrix.


### -field _12

The value in the first row and second column of the matrix.


### -field _21

The value in the second row and first column of the matrix.


### -field _22

The value in the second row and second column of the matrix.


### -field _31

The value in the third row and first column of the matrix.


### -field _32

The value in the third row and second column of the matrix.


## -see-also




<a href="https://msdn.microsoft.com/22e98880-bcd1-448a-9223-604fff9173fe">DXGI Structures</a>
 

 

