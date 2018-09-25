---
UID: NF:d2d1helper.operator-mult
title: operator* function
author: windows-sdk-content
description: Multiplies two matrices and returns the result.
old-location: direct2d\operator__const__amp_d2d1_matrix_3x2_f_const__amp_d2d1_matrix_3x2_f_.htm
tech.root: direct2d
ms.assetid: ba810ab8-53fe-4c7d-8e47-043ae57e4323
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: direct2d.operator__const__amp_d2d1_matrix_3x2_f_const__amp_d2d1_matrix_3x2_f_, operator*, operator* function [Direct2D], operator*(const D2D1_MATRIX_3X2_F&,const D2D1_MATRIX_3X2_F&), windowsnumerics/operator*
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: d2d1helper.h
req.include-header: D2d1helper.h, D3dvec.inl
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
 - operator*
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# operator* function


## -description


Multiplies two matrices and returns the result.


## -parameters




### -param point [ref]

Type: <b>const <a href="https://msdn.microsoft.com/f05d7555-6482-4eea-950f-7b443892cc1f">D2D1_MATRIX_3X2_F</a></b>

The first matrix to multiply.


### -param matrix [ref]

Type: <b>const <a href="https://msdn.microsoft.com/f05d7555-6482-4eea-950f-7b443892cc1f">D2D1_MATRIX_3X2_F</a></b>

The second matrix to multiply.


## -returns



Type: <b><a href="https://msdn.microsoft.com/f05d7555-6482-4eea-950f-7b443892cc1f">D2D1_MATRIX_3X2_F</a></b>

The result of multiplying <i>matrix1</i> and <i>matrix2</i>.



