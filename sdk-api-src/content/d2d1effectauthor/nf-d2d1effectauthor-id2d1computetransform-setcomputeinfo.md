---
UID: NF:d2d1effectauthor.ID2D1ComputeTransform.SetComputeInfo
title: ID2D1ComputeTransform::SetComputeInfo (d2d1effectauthor.h)
description: Sets the render information used to specify the compute shader pass.
helpviewer_keywords: ["ID2D1ComputeTransform interface [Direct2D]","SetComputeInfo method","ID2D1ComputeTransform.SetComputeInfo","ID2D1ComputeTransform::SetComputeInfo","SetComputeInfo","SetComputeInfo method [Direct2D]","SetComputeInfo method [Direct2D]","ID2D1ComputeTransform interface","d2d1effectauthor/ID2D1ComputeTransform::SetComputeInfo","direct2d.id2d1computetransform_setrenderinfo"]
old-location: direct2d\id2d1computetransform_setrenderinfo.htm
tech.root: Direct2D
ms.assetid: 9FDA98A0-90DC-47A5-8839-33606A12C700
ms.date: 12/05/2018
ms.keywords: ID2D1ComputeTransform interface [Direct2D],SetComputeInfo method, ID2D1ComputeTransform.SetComputeInfo, ID2D1ComputeTransform::SetComputeInfo, SetComputeInfo, SetComputeInfo method [Direct2D], SetComputeInfo method [Direct2D],ID2D1ComputeTransform interface, d2d1effectauthor/ID2D1ComputeTransform::SetComputeInfo, direct2d.id2d1computetransform_setrenderinfo
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
 - ID2D1ComputeTransform::SetComputeInfo
 - d2d1effectauthor/ID2D1ComputeTransform::SetComputeInfo
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
 - ID2D1ComputeTransform.SetComputeInfo
---

# ID2D1ComputeTransform::SetComputeInfo


## -description

Sets the render information used to specify the compute shader pass.

## -parameters

### -param computeInfo [in]

Type: <b><a href="/windows/desktop/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1computeinfo">ID2D1ComputeInfo</a>*</b>

The render information object to set.

## -returns

Type: <b>HRESULT</b>

If the method succeeds, it returns <b>S_OK</b>. If it fails, it returns an <b>HRESULT</b> error code.

## -remarks

If this method fails, <a href="/windows/desktop/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transformgraph-addnode">ID2D1TransformGraph::AddNode</a> fails.

## -see-also

<a href="/windows/desktop/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1computetransform">ID2D1ComputeTransform</a>



<a href="/windows/desktop/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-loadcomputeshader">ID2D1EffectContext::LoadComputeShader</a>