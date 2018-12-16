---
UID: NF:d2d1.ID2D1RenderTarget.CreateLayer(D2D1_SIZE_F,ID2D1Layer)
title: ID2D1RenderTarget::CreateLayer(D2D1_SIZE_F,ID2D1Layer)
author: windows-sdk-content
description: Creates a layer resource that can be used with this render target and its compatible render targets. The new layer has the specified initial size.
old-location: direct2d\ID2D1RenderTarget_CreateLayer_D2D_SIZE_F_ptr_ptr_ID2D1Layer.htm
tech.root: direct2d
ms.assetid: c21596a3-2b10-4a96-9a01-cf9325e51fe3
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CreateLayer, CreateLayer method [Direct2D], CreateLayer method [Direct2D],ID2D1RenderTarget interface, ID2D1RenderTarget interface [Direct2D],CreateLayer method, ID2D1RenderTarget.CreateLayer, ID2D1RenderTarget.CreateLayer(D2D1_SIZE_F,ID2D1Layer), ID2D1RenderTarget::CreateLayer, ID2D1RenderTarget::CreateLayer(D2D1_SIZE_F,ID2D1Layer), d2d1/ID2D1RenderTarget::CreateLayer, direct2d.ID2D1RenderTarget_CreateLayer_D2D_SIZE_F_ptr_ptr_ID2D1Layer
ms.topic: method
req.header: d2d1.h
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2d1.dll
api_name:
 - ID2D1RenderTarget.CreateLayer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1RenderTarget::CreateLayer(D2D1_SIZE_F,ID2D1Layer)


## -description


Creates a layer resource that can be used with this render target and its compatible render targets. The new layer has the specified initial size. 


## -parameters




### -param size

Type: <b><a href="https://msdn.microsoft.com/c2fd41fb-72b3-418b-ad87-65549b04657d">D2D1_SIZE_F</a></b>

If (0, 0) is specified, no backing store is created behind the layer resource. The layer resource is allocated to the minimum size when <a href="https://msdn.microsoft.com/905e9c76-d09e-4df8-8343-520d856ec6b8">PushLayer</a> is called.


### -param layer [out]

Type: <b><a href="https://msdn.microsoft.com/ce7b2345-f0e5-4e44-9146-b1f140bb00ca">ID2D1Layer</a>**</b>

When the method returns, contains a pointer to a pointer to the new layer. This parameter is passed uninitialized.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Regardless of whether a size is initially specified, the layer automatically resizes as needed.


#### Examples

For an example on how to use <a href="https://msdn.microsoft.com/074e9ffb-c5f2-4e7b-94c7-d457bf07c0b7">CreateLayer</a>, see the <a href="https://msdn.microsoft.com/eaeb6cfd-de62-46f1-972d-a11e0ccc11d9">How to Clip a Region with a Layer</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/40629be9-5840-4bde-b369-56bbfd791775">ID2D1RenderTarget</a>



<a href="https://msdn.microsoft.com/22d161fb-8470-49cc-a523-309f90643ea9">Layers Overview</a>
 

 

