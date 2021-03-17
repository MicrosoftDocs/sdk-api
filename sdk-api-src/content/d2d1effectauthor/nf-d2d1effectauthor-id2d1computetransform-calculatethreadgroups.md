---
UID: NF:d2d1effectauthor.ID2D1ComputeTransform.CalculateThreadgroups
title: ID2D1ComputeTransform::CalculateThreadgroups (d2d1effectauthor.h)
description: This method allows a compute-shader–based transform to select the number of thread groups to execute based on the number of output pixels it needs to fill.
helpviewer_keywords: ["CalculateThreadgroups","CalculateThreadgroups method [Direct2D]","CalculateThreadgroups method [Direct2D]","ID2D1ComputeTransform interface","ID2D1ComputeTransform interface [Direct2D]","CalculateThreadgroups method","ID2D1ComputeTransform.CalculateThreadgroups","ID2D1ComputeTransform::CalculateThreadgroups","d2d1effectauthor/ID2D1ComputeTransform::CalculateThreadgroups","direct2d.id2d1computetransform_calculatethreadgroups"]
old-location: direct2d\id2d1computetransform_calculatethreadgroups.htm
tech.root: Direct2D
ms.assetid: 6B662297-3EBE-459F-8284-7A59F67DB025
ms.date: 12/05/2018
ms.keywords: CalculateThreadgroups, CalculateThreadgroups method [Direct2D], CalculateThreadgroups method [Direct2D],ID2D1ComputeTransform interface, ID2D1ComputeTransform interface [Direct2D],CalculateThreadgroups method, ID2D1ComputeTransform.CalculateThreadgroups, ID2D1ComputeTransform::CalculateThreadgroups, d2d1effectauthor/ID2D1ComputeTransform::CalculateThreadgroups, direct2d.id2d1computetransform_calculatethreadgroups
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
req.type-library: 
req.lib: D2d1.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID2D1ComputeTransform::CalculateThreadgroups
 - d2d1effectauthor/ID2D1ComputeTransform::CalculateThreadgroups
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d2d1.lib
 - d2d1.dll
api_name:
 - ID2D1ComputeTransform.CalculateThreadgroups
---

# ID2D1ComputeTransform::CalculateThreadgroups


## -description

This method allows a compute-shader–based transform to select the number of thread groups to execute based on the number of output pixels it needs to fill.

## -parameters

### -param outputRect [in]

Type: <b>const <a href="/previous-versions/windows/desktop/legacy/hh847950(v=vs.85)">D2D1_RECT_L</a>*</b>

The output rectangle that will be filled by the compute transform.

### -param dimensionX [out]

Type: <b>UINT32*</b>

The number of threads in the x dimension.

### -param dimensionY [out]

Type: <b>UINT32*</b>

The number of threads in the y dimension.

### -param dimensionZ [out]

Type: <b>UINT32*</b>

The number of threads in the z dimension.

## -returns

Type: <b>HRESULT</b>

If the method succeeds, it returns <b>S_OK</b>. If it fails, it returns an <b>HRESULT</b> error code.

## -remarks

If this call fails, the corresponding <a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect">ID2D1Effect</a> instance is placed into an error state and fails to draw.

## -see-also

<a href="/windows/desktop/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1computetransform">ID2D1ComputeTransform</a>



<a href="/windows/desktop/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-loadcomputeshader">ID2D1EffectContext::LoadComputeShader</a>