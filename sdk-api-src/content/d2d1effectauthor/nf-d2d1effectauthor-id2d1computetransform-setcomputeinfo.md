---
UID: NF:d2d1effectauthor.ID2D1ComputeTransform.SetComputeInfo
title: ID2D1ComputeTransform::SetComputeInfo
author: windows-sdk-content
description: Sets the render information used to specify the compute shader pass.
old-location: direct2d\id2d1computetransform_setrenderinfo.htm
tech.root: direct2d
ms.assetid: 9FDA98A0-90DC-47A5-8839-33606A12C700
ms.author: windowssdkdev
ms.date: 10/17/2018
ms.keywords: ID2D1ComputeTransform interface [Direct2D],SetComputeInfo method, ID2D1ComputeTransform.SetComputeInfo, ID2D1ComputeTransform::SetComputeInfo, SetComputeInfo, SetComputeInfo method [Direct2D], SetComputeInfo method [Direct2D],ID2D1ComputeTransform interface, d2d1effectauthor/ID2D1ComputeTransform::SetComputeInfo, direct2d.id2d1computetransform_setrenderinfo
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1ComputeTransform::SetComputeInfo


## -description


Sets the render information used to specify the compute shader pass.


## -parameters




### -param computeInfo [in]

Type: <b><a href="https://msdn.microsoft.com/0560BB4B-B837-4DA8-AD68-545224152BA5">ID2D1ComputeInfo</a>*</b>

The render information object to set.


## -returns



Type: <b>HRESULT</b>

If the method succeeds, it returns <b>S_OK</b>. If it fails, it returns an <b>HRESULT</b> error code.




## -remarks



If this method fails, <a href="https://msdn.microsoft.com/1937BD5F-C26A-4E67-8E07-688A24DA201E">ID2D1TransformGraph::AddNode</a> fails.




## -see-also




<a href="https://msdn.microsoft.com/2D7B82E1-6EB7-492A-B65C-CE5EFBFACC31">ID2D1ComputeTransform</a>



<a href="https://msdn.microsoft.com/64CA9647-8E9E-417D-A8D4-71AAF58F1C32">ID2D1EffectContext::LoadComputeShader</a>
 

 

