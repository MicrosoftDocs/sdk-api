---
UID: NF:d2d1_1.ID2D1CommandSink.SetTransform
title: ID2D1CommandSink::SetTransform
author: windows-sdk-content
description: Sets a new transform.
old-location: direct2d\id2d1commandsink_settransform.htm
tech.root: Direct2D
ms.assetid: bc284b13-cf22-45aa-b80c-0750622f5284
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: ID2D1CommandSink interface [Direct2D],SetTransform method, ID2D1CommandSink.SetTransform, ID2D1CommandSink::SetTransform, SetTransform, SetTransform method [Direct2D], SetTransform method [Direct2D],ID2D1CommandSink interface, d2d1_1/ID2D1CommandSink::SetTransform, direct2d.id2d1commandsink_settransform
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d2d1_1.h
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
req.lib: 
req.dll: D2d1.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2d1.dll
api_name:
 - ID2D1CommandSink.SetTransform
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1CommandSink::SetTransform


## -description


Sets a new transform.


## -parameters




### -param transform [in]

Type: <b>const <a href="https://msdn.microsoft.com/f05d7555-6482-4eea-950f-7b443892cc1f">D2D1_MATRIX_3X2_F</a>*</b>

The transform to be set.


## -returns



Type: <b>HRESULT</b>

If the method succeeds, it returns <b>S_OK</b>. If it fails, it returns an <b>HRESULT</b> error code. 





## -remarks



The transform will be applied to the corresponding device context.




## -see-also




<a href="https://msdn.microsoft.com/52e6da86-c7c6-48e7-b0ff-a54770663f14">ID2D1CommandList::Stream</a>



<a href="https://msdn.microsoft.com/4e0ce837-7f4e-4b93-8dd7-68f60cfb1105">ID2D1CommandSink</a>



<a href="https://msdn.microsoft.com/04799366-6458-40ff-a2fb-5d227eab041d">ID2D1RenderTarget::SetTransform</a>
 

 

