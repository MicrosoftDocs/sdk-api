---
UID: NF:d2d1_1.ID2D1CommandSink.SetPrimitiveBlend
title: ID2D1CommandSink::SetPrimitiveBlend
author: windows-sdk-content
description: Sets a new primitive blend mode.
old-location: direct2d\id2d1commandsink_setprimitiveblend.htm
tech.root: direct2d
ms.assetid: 80b7047f-1200-4dc9-bc64-96678524a449
ms.author: windowssdkdev
ms.date: 10/25/2018
ms.keywords: ID2D1CommandSink interface [Direct2D],SetPrimitiveBlend method, ID2D1CommandSink.SetPrimitiveBlend, ID2D1CommandSink::SetPrimitiveBlend, SetPrimitiveBlend, SetPrimitiveBlend method [Direct2D], SetPrimitiveBlend method [Direct2D],ID2D1CommandSink interface, d2d1_1/ID2D1CommandSink::SetPrimitiveBlend, direct2d.id2d1commandsink_setprimitiveblend
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
 - ID2D1CommandSink.SetPrimitiveBlend
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1CommandSink::SetPrimitiveBlend


## -description


Sets a new primitive blend mode.


## -parameters




### -param primitiveBlend

Type: <b><a href="https://msdn.microsoft.com/411a42c9-f8d7-46f3-a6e6-51afc83375ad">D2D1_PRIMITIVE_BLEND</a></b>

The primitive blend that will apply to subsequent primitives.


## -returns



Type: <b>HRESULT</b>

If the method succeeds, it returns <b>S_OK</b>. If it fails, it returns an <b>HRESULT</b> error code. 





## -see-also




<a href="https://msdn.microsoft.com/52e6da86-c7c6-48e7-b0ff-a54770663f14">ID2D1CommandList::Stream</a>



<a href="https://msdn.microsoft.com/4e0ce837-7f4e-4b93-8dd7-68f60cfb1105">ID2D1CommandSink</a>



<a href="https://msdn.microsoft.com/04799366-6458-40ff-a2fb-5d227eab041d">ID2D1RenderTarget::SetTransform</a>
 

 

