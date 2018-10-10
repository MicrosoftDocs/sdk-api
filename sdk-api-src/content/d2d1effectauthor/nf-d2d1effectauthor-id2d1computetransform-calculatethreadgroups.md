---
UID: NF:d2d1effectauthor.ID2D1ComputeTransform.CalculateThreadgroups
title: ID2D1ComputeTransform::CalculateThreadgroups
author: windows-sdk-content
description: This method allows a compute-shader–based transform to select the number of thread groups to execute based on the number of output pixels it needs to fill.
old-location: direct2d\id2d1computetransform_calculatethreadgroups.htm
tech.root: Direct2D
ms.assetid: 6B662297-3EBE-459F-8284-7A59F67DB025
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: CalculateThreadgroups, CalculateThreadgroups method [Direct2D], CalculateThreadgroups method [Direct2D],ID2D1ComputeTransform interface, ID2D1ComputeTransform interface [Direct2D],CalculateThreadgroups method, ID2D1ComputeTransform.CalculateThreadgroups, ID2D1ComputeTransform::CalculateThreadgroups, d2d1effectauthor/ID2D1ComputeTransform::CalculateThreadgroups, direct2d.id2d1computetransform_calculatethreadgroups
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
 - ID2D1ComputeTransform.CalculateThreadgroups
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1ComputeTransform::CalculateThreadgroups


## -description


This method allows a compute-shader–based transform to select the number of thread groups to execute based on the number of output pixels it needs to fill.


## -parameters




### -param outputRect [in]

Type: <b>const <a href="https://msdn.microsoft.com/655EBC1A-199E-40A2-A4C2-9622AFAEE0B5">D2D1_RECT_L</a>*</b>

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



If this call fails, the corresponding <a href="https://msdn.microsoft.com/e90d1830-c356-48f1-ac7b-1d94c8c26569">ID2D1Effect</a> instance is placed into an error state and fails to draw.




## -see-also




<a href="https://msdn.microsoft.com/2D7B82E1-6EB7-492A-B65C-CE5EFBFACC31">ID2D1ComputeTransform</a>



<a href="https://msdn.microsoft.com/64CA9647-8E9E-417D-A8D4-71AAF58F1C32">ID2D1EffectContext::LoadComputeShader</a>
 

 

