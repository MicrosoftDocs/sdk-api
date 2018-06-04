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

# D2D1_COLORMATRIX_PROP enumeration


## -description


Identifiers for the properties of the <a href="https://msdn.microsoft.com/093EEEF1-8C38-414E-8261-58A6C3DD930D">Color matrix effect</a>.


## -enum-fields




### -field D2D1_COLORMATRIX_PROP_COLOR_MATRIX

A 5x4 matrix of float values. The elements in the matrix are not bounded and are unitless.
          

The type is <a href="https://msdn.microsoft.com/c6f57691-1530-e57a-c1b4-b68b4d8967e3">D2D1_MATRIX_5X4_F</a>.

The default value is the identity matrix, Matrix5x4F(1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 0, 0).


### -field D2D1_COLORMATRIX_PROP_ALPHA_MODE

The alpha mode of the output. 
          

The type is <a href="https://msdn.microsoft.com/7D7CB142-5758-4745-A4CD-41B3E2465562">D2D1_COLORMATRIX_ALPHA_MODE</a>.

The default value is D2D1_COLORMATRIX_ALPHA_MODE_PREMULTIPLIED.


### -field D2D1_COLORMATRIX_PROP_CLAMP_OUTPUT

Whether the effect clamps color values to between 0 and 1 before the effect passes the values to the next effect in the graph. 
          The effect clamps the values before it premultiplies the alpha.
          

If you set this to TRUE the effect will clamp the values. If you set this to FALSE, the effect will not clamp the color values, 
          but other effects and the output surface may clamp the values if they are not of high enough precision.

The type is BOOL.

The default value is FALSE.


### -field D2D1_COLORMATRIX_PROP_FORCE_DWORD



