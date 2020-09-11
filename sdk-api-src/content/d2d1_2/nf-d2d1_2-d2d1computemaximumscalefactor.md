---
UID: NF:d2d1_2.D2D1ComputeMaximumScaleFactor
title: D2D1ComputeMaximumScaleFactor function (d2d1_2.h)
description: Computes the maximum factor by which a given transform can stretch any vector.
helpviewer_keywords: ["D2D1ComputeMaximumScaleFactor","D2D1ComputeMaximumScaleFactor function [Direct2D]","d2d1_2/D2D1ComputeMaximumScaleFactor","direct2d.d2d1computemaximumscalefactor"]
old-location: direct2d\d2d1computemaximumscalefactor.htm
tech.root: Direct2D
ms.assetid: 5BC10305-436F-4528-9647-E70713130505
ms.date: 12/05/2018
ms.keywords: D2D1ComputeMaximumScaleFactor, D2D1ComputeMaximumScaleFactor function [Direct2D], d2d1_2/D2D1ComputeMaximumScaleFactor, direct2d.d2d1computemaximumscalefactor
req.header: d2d1_2.h
req.include-header: D2d1_1.h
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
req.lib: D2d1.lib
req.dll: D2d1.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D2D1ComputeMaximumScaleFactor
 - d2d1_2/D2D1ComputeMaximumScaleFactor
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
 - D2D1ComputeMaximumScaleFactor
---

# D2D1ComputeMaximumScaleFactor function


## -description

Computes the maximum factor by which a given transform can stretch any vector.

## -parameters

### -param matrix [in]

The input transform matrix.

## -returns

The scale factor.

## -remarks

Formally, if M is the input matrix, this method will return the maximum value of |V * M| / |V| for all vectors V, where |.| denotes length.



<div class="alert"><b>Note</b>  Since this describes how M affects vectors (rather than points), the translation components (_31 and _32) of M are ignored.</div>
<div> </div>

