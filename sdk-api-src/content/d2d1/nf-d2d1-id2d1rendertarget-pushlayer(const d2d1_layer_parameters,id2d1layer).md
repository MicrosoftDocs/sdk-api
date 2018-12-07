---
UID: NF:d2d1.ID2D1RenderTarget.PushLayer(const D2D1_LAYER_PARAMETERS,ID2D1Layer)
title: ID2D1RenderTarget::PushLayer(const D2D1_LAYER_PARAMETERS,ID2D1Layer)
author: windows-sdk-content
description: Adds the specified layer to the render target so that it receives all subsequent drawing operations until PopLayer is called.
old-location: direct2d\ID2D1RenderTarget_PushLayer_ptr_D2D1_LAYER_PARAMETERS_ptr_ID2D1Layer.htm
tech.root: Direct2D
ms.assetid: 0fc7ac38-ff74-4f3b-9aa2-025a99e6b013
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: ID2D1RenderTarget interface [Direct2D],PushLayer method, ID2D1RenderTarget.PushLayer, ID2D1RenderTarget.PushLayer(const D2D1_LAYER_PARAMETERS,ID2D1Layer), ID2D1RenderTarget::PushLayer, ID2D1RenderTarget::PushLayer(const D2D1_LAYER_PARAMETERS,ID2D1Layer), PushLayer, PushLayer method [Direct2D], PushLayer method [Direct2D],ID2D1RenderTarget interface, d2d1/ID2D1RenderTarget::PushLayer, direct2d.ID2D1RenderTarget_PushLayer_ptr_D2D1_LAYER_PARAMETERS_ptr_ID2D1Layer
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
 - ID2D1RenderTarget.PushLayer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- d2d1.h
: 
- ID2D1RenderTarget.PushLayer
: 
---

# ID2D1RenderTarget::PushLayer(const D2D1_LAYER_PARAMETERS,ID2D1Layer)


## -description


Adds the specified layer to the render target so that it receives all subsequent drawing operations until <a href="https://msdn.microsoft.com/6ab05160-4f42-477f-a5bf-f16863b0635c">PopLayer</a> is called. 


## -parameters




### -param layerParameters [in]

Type: <b>const <a href="https://msdn.microsoft.com/ce575df6-9464-4672-9a0e-ff7e016d9354">D2D1_LAYER_PARAMETERS</a>*</b>

The content bounds, geometric mask, opacity, opacity mask, and antialiasing options for the layer. 


### -param layer [in]

Type: <b><a href="https://msdn.microsoft.com/ce7b2345-f0e5-4e44-9146-b1f140bb00ca">ID2D1Layer</a>*</b>

The layer that receives subsequent drawing operations.

<div class="alert"><b>Note</b>  Starting with Windows 8, this parameter is optional. If a layer is not specified, Direct2D manages the layer resource automatically.</div>
<div> </div>

## -returns



This method does not return a value.




## -remarks



The <a href="https://msdn.microsoft.com/905e9c76-d09e-4df8-8343-520d856ec6b8">PushLayer</a> method allows a caller to begin redirecting rendering to a layer. All rendering operations are valid in a layer. The location of the layer is affected by the world transform set on the render target. 

Each <a href="https://msdn.microsoft.com/9336662c-e94e-40ba-adbe-066d704958bc">PushLayer</a> must have a matching <a href="https://msdn.microsoft.com/6ab05160-4f42-477f-a5bf-f16863b0635c">PopLayer</a> call. If there are more <b>PopLayer</b> calls than <b>PushLayer</b> calls, the render target is placed into an error state. If <a href="https://msdn.microsoft.com/3ad9c966-85f5-4ddb-a8c1-aefcba533509">Flush</a> is called before all outstanding layers are popped, the render target is placed into an error state, and an error is returned. The error state can be cleared by a call to <a href="https://msdn.microsoft.com/a8f24501-4e85-4981-bb38-2bd6333a7b49">EndDraw</a>.

A particular <a href="https://msdn.microsoft.com/ce7b2345-f0e5-4e44-9146-b1f140bb00ca">ID2D1Layer</a> resource can be active only at one time. In other words, you cannot call a <a href="https://msdn.microsoft.com/905e9c76-d09e-4df8-8343-520d856ec6b8">PushLayer</a> method, and then  immediately follow with another <b>PushLayer</b> method with the same layer resource. Instead, you must call the second <b>PushLayer</b> method with different layer resources. 


This method doesn't return an error code if it fails. To determine whether a drawing operation (such as <a href="https://msdn.microsoft.com/9336662c-e94e-40ba-adbe-066d704958bc">PushLayer</a>) failed, check the result returned by the <a href="https://msdn.microsoft.com/a8f24501-4e85-4981-bb38-2bd6333a7b49">ID2D1RenderTarget::EndDraw</a> or <a href="https://msdn.microsoft.com/3ad9c966-85f5-4ddb-a8c1-aefcba533509">ID2D1RenderTarget::Flush</a> methods. 




## -see-also




<a href="https://msdn.microsoft.com/40629be9-5840-4bde-b369-56bbfd791775">ID2D1RenderTarget</a>



<a href="https://msdn.microsoft.com/22d161fb-8470-49cc-a523-309f90643ea9">Layers Overview</a>



<a href="https://msdn.microsoft.com/6ab05160-4f42-477f-a5bf-f16863b0635c">PopLayer</a>
 

 

