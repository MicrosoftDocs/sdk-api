---
UID: NF:d2d1.ID2D1RenderTarget.CreateLayer(ID2D1Layer)
title: ID2D1RenderTarget::CreateLayer(ID2D1Layer)
author: windows-sdk-content
description: Creates a layer resource that can be used with this render target and its compatible render targets.
old-location: direct2d\ID2D1RenderTarget_CreateLayer_ptr_ptr_ID2D1Layer.htm
tech.root: Direct2D
ms.assetid: 6a3377fb-f847-454f-9716-70a7b65fe96c
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: CreateLayer, CreateLayer method [Direct2D], CreateLayer method [Direct2D],ID2D1RenderTarget interface, ID2D1RenderTarget interface [Direct2D],CreateLayer method, ID2D1RenderTarget.CreateLayer, ID2D1RenderTarget.CreateLayer(ID2D1Layer), ID2D1RenderTarget::CreateLayer, ID2D1RenderTarget::CreateLayer(ID2D1Layer), d2d1/ID2D1RenderTarget::CreateLayer, direct2d.ID2D1RenderTarget_CreateLayer_ptr_ptr_ID2D1Layer
ms.prod: windows-hardware
ms.technology: windows-devices
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

# ID2D1RenderTarget::CreateLayer(ID2D1Layer)


## -description


Creates a layer resource that can be used with this render target and its compatible render targets. 


## -parameters




### -param layer [out]

Type: <b><a href="https://msdn.microsoft.com/ce7b2345-f0e5-4e44-9146-b1f140bb00ca">ID2D1Layer</a>**</b>

When the method returns, contains a pointer to a pointer to the new layer. This parameter is passed uninitialized.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The layer automatically resizes itself, as needed.  


#### Examples

For an example on how to use <a href="https://msdn.microsoft.com/074e9ffb-c5f2-4e7b-94c7-d457bf07c0b7">CreateLayer</a>, see the <a href="https://msdn.microsoft.com/eaeb6cfd-de62-46f1-972d-a11e0ccc11d9">How to Clip a Region with a Layer</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/40629be9-5840-4bde-b369-56bbfd791775">ID2D1RenderTarget</a>



<a href="https://msdn.microsoft.com/22d161fb-8470-49cc-a523-309f90643ea9">Layers Overview</a>
 

 

