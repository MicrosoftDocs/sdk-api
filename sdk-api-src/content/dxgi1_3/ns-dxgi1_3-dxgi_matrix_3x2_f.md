---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

