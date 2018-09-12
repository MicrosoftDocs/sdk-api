---
UID: NE:d2d1effectauthor.D2D1_BLEND_OPERATION
title: D2D1_BLEND_OPERATION
author: windows-sdk-content
description: Specifies the blend operation on two color sources.
old-location: direct2d\d2d1_blend_operation.htm
tech.root: direct2d
ms.assetid: 54977cf3-cca3-4a1e-a039-1ee4a8d44686
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: D2D1_BLEND_OPERATION, D2D1_BLEND_OPERATION enumeration [Direct2D], D2D1_BLEND_OPERATION_ADD, D2D1_BLEND_OPERATION_MAX, D2D1_BLEND_OPERATION_MIN, D2D1_BLEND_OPERATION_REV_SUBSTRACT, D2D1_BLEND_OPERATION_SUBTRACT, d2d1effectauthor/D2D1_BLEND_OPERATION, d2d1effectauthor/D2D1_BLEND_OPERATION_ADD, d2d1effectauthor/D2D1_BLEND_OPERATION_MAX, d2d1effectauthor/D2D1_BLEND_OPERATION_MIN, d2d1effectauthor/D2D1_BLEND_OPERATION_REV_SUBSTRACT, d2d1effectauthor/D2D1_BLEND_OPERATION_SUBTRACT, direct2d.d2d1_blend_operation
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: d2d1effectauthor.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: D2d1.lib; D2d1.dll
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - LibDef
api_location:
 - D2d1.lib
 - D2d1.dll
api_name:
 - D2D1_BLEND_OPERATION
product: Windows
targetos: Windows
req.typenames: D2D1_BLEND_OPERATION
req.redist: 
---

# D2D1_BLEND_OPERATION enumeration


## -description


Specifies the blend operation on two color sources.


## -enum-fields




### -field D2D1_BLEND_OPERATION_ADD

Add source 1 and source 2.


### -field D2D1_BLEND_OPERATION_SUBTRACT

Subtract source 1 from source 2.


### -field D2D1_BLEND_OPERATION_REV_SUBTRACT


### -field D2D1_BLEND_OPERATION_MIN

Find the minimum of source 1 and source 2.


### -field D2D1_BLEND_OPERATION_MAX

Find the maximum of source 1 and source 2.


### -field D2D1_BLEND_OPERATION_FORCE_DWORD




#### - D2D1_BLEND_OPERATION_REV_SUBSTRACT

Subtract source 2 from source 1.


## -remarks



This enumeration has the same numeric values as <a href="https://msdn.microsoft.com/en-us/library/Bb204894(v=VS.85).aspx">D3D10_BLEND_OP</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Hh404277(v=VS.85).aspx">D2D1_BLEND_DESCRIPTION</a>



<a href="https://msdn.microsoft.com/0DC46758-6005-4A33-9539-9C95CF8CFB6A">ID2D1BlendTransform</a>
 

 

