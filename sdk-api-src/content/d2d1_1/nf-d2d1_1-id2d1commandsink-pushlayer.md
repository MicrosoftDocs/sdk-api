---
UID: NF:d2d1_1.ID2D1CommandSink.PushLayer
title: ID2D1CommandSink::PushLayer
author: windows-sdk-content
description: Pushes a layer onto the clip and layer stack.
old-location: direct2d\id2d1commandsink_pushlayer.htm
tech.root: direct2d
ms.assetid: 071d7d7a-12d7-4611-812c-103e2b9a5e56
ms.author: windowssdkdev
ms.date: 11/13/2018
ms.keywords: ID2D1CommandSink interface [Direct2D],PushLayer method, ID2D1CommandSink.PushLayer, ID2D1CommandSink::PushLayer, PushLayer, PushLayer method [Direct2D], PushLayer method [Direct2D],ID2D1CommandSink interface, d2d1_1/ID2D1CommandSink::PushLayer, direct2d.id2d1commandsink_pushlayer
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
 - ID2D1CommandSink.PushLayer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- d2d1_1.h
: 
- ID2D1CommandSink.PushLayer
: 
---

# ID2D1CommandSink::PushLayer


## -description


Pushes a layer onto the clip and layer stack.


## -parameters




### -param layerParameters1

TBD


### -param layer [in]

Type: <b><a href="https://msdn.microsoft.com/ce7b2345-f0e5-4e44-9146-b1f140bb00ca">ID2D1Layer</a>*</b>

The layer resource that receives subsequent drawing operations.


#### - layerParameters [in]

Type: <b>const <a href="https://msdn.microsoft.com/ce575df6-9464-4672-9a0e-ff7e016d9354">D2D1_LAYER_PARAMETERS1</a>*</b>

The parameters that define the layer.


## -returns



Type: <b>HRESULT</b>

If the method succeeds, it returns <b>S_OK</b>. If it fails, it returns an <b>HRESULT</b> error code. 





## -see-also




<a href="https://msdn.microsoft.com/52e6da86-c7c6-48e7-b0ff-a54770663f14">ID2D1CommandList::Stream</a>



<a href="https://msdn.microsoft.com/4e0ce837-7f4e-4b93-8dd7-68f60cfb1105">ID2D1CommandSink</a>



<a href="https://msdn.microsoft.com/8b777425-07b1-4494-889a-0c947fb61315">ID2D1RenderTarget::PushAxisAlignedClip</a>
 

 

