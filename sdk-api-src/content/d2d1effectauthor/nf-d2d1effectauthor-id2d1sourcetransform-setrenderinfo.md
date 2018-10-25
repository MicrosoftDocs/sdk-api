---
UID: NF:d2d1effectauthor.ID2D1SourceTransform.SetRenderInfo
title: ID2D1SourceTransform::SetRenderInfo
author: windows-sdk-content
description: Sets the render information for the transform.
old-location: direct2d\id2d1sourcetransform_setrenderinfo.htm
tech.root: direct2d
ms.assetid: 7082A748-E1DF-4805-BBB5-9EF50841B36D
ms.author: windowssdkdev
ms.date: 10/24/2018
ms.keywords: ID2D1SourceTransform interface [Direct2D],SetRenderInfo method, ID2D1SourceTransform.SetRenderInfo, ID2D1SourceTransform::SetRenderInfo, SetRenderInfo, SetRenderInfo method [Direct2D], SetRenderInfo method [Direct2D],ID2D1SourceTransform interface, d2d1effectauthor/ID2D1SourceTransform::SetRenderInfo, direct2d.id2d1sourcetransform_setrenderinfo
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
 - ID2D1SourceTransform.SetRenderInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1SourceTransform::SetRenderInfo


## -description


Sets the render information for the transform.


## -parameters




### -param renderInfo [in]

Type: <b><a href="https://msdn.microsoft.com/26FB6D27-7EE0-43DA-A575-D9FF77846A16">ID2D1RenderInfo</a>*</b>

The interface supplied to the transform to allow specifying the CPU based transform pass.


## -returns



Type: <b>HRESULT</b>

If the method succeeds, it returns <b>S_OK</b>. If it fails, it returns an <b>HRESULT</b> error code.




## -remarks



Provides a render information interface to the source transform to allow it to specify state to the rendering system.




## -see-also




<a href="https://msdn.microsoft.com/3D87A908-FC57-4AA9-A508-C402D8413363">ID2D1EffectImpl</a>



<a href="https://msdn.microsoft.com/A2B3E8E1-8F7F-4AFA-B1CE-5E8A5FCD9B70">ID2D1SourceTransform</a>
 

 

