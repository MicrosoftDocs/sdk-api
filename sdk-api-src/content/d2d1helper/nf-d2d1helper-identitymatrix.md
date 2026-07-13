---
UID: NF:d2d1helper.IdentityMatrix
title: IdentityMatrix function (d2d1helper.h)
description: Creates an identity matrix. (IdentityMatrix)
helpviewer_keywords: ["IdentityMatrix","IdentityMatrix function [Direct2D]","d2d1helper/IdentityMatrix","direct2d.identitymatrix"]
old-location: direct2d\identitymatrix.htm
tech.root: Direct2D
ms.assetid: 09c2ed59-db4a-4753-a98a-bef7748d3803
ms.date: 12/05/2018
ms.keywords: IdentityMatrix, IdentityMatrix function [Direct2D], d2d1helper/IdentityMatrix, direct2d.identitymatrix
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IdentityMatrix
 - d2d1helper/IdentityMatrix
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - D2d1.dll
api_name:
 - IdentityMatrix
---

# IdentityMatrix function


## -description

Creates an identity matrix.



## -returns

Type: <b><a href="/windows/desktop/Direct2D/d2d1-matrix-3x2-f">D2D1_MATRIX_3X2_F</a></b>

An identity matrix.

## -remarks

The identity matrix is the 3x2 matrix with ones on the main diagonal and zeros elsewhere. When an identity transform is applied to an object, it does not change the position, shape, or size of the object. It is similar to the way that multiplying a number by 1 does not change the number. Any transform other than the identity transform will modify the position, shape, and/or size of objects.



Calling this function is the same as calling <a href="/windows/desktop/api/d2d1helper/nf-d2d1helper-matrix3x2f-identity">D2D1::Matrix3x2F::Identity()</a>.

## -see-also

<a href="/windows/desktop/Direct2D/d2d1-matrix-3x2-f">D2D1_MATRIX_3X2_F</a>
