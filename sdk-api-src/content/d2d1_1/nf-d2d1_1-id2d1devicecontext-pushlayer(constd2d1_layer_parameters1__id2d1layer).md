---
UID: NF:d2d1_1.ID2D1DeviceContext.PushLayer(const D2D1_LAYER_PARAMETERS1 &,ID2D1Layer)
title: ID2D1DeviceContext::PushLayer(const D2D1_LAYER_PARAMETERS1 &,ID2D1Layer) (d2d1_1.h)
author: windows-sdk-content
description: Push a layer onto the clip and layer stack of the device context.
old-location: direct2d\id2d1devicecontext_pushlayer.htm
tech.root: Direct2D
ms.assetid: 7DC719E3-CE94-4B7F-B02D-62D78425CFFE
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ID2D1DeviceContext interface [Direct2D],PushLayer method, ID2D1DeviceContext.PushLayer, ID2D1DeviceContext.PushLayer(const D2D1_LAYER_PARAMETERS1 &,ID2D1Layer), ID2D1DeviceContext::PushLayer, ID2D1DeviceContext::PushLayer(const D2D1_LAYER_PARAMETERS1 &,ID2D1Layer), PushLayer, PushLayer method [Direct2D], PushLayer method [Direct2D],ID2D1DeviceContext interface, d2d1_1/ID2D1DeviceContext::PushLayer, direct2d.id2d1devicecontext_pushlayer
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
 - ID2D1DeviceContext.PushLayer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1DeviceContext::PushLayer(const D2D1_LAYER_PARAMETERS1 &,ID2D1Layer)


## -description


Push a layer onto the clip and layer stack of the device context.


## -parameters




### -param layerParameters [in]

Type: <b>const <a href="https://msdn.microsoft.com/D7CC93F8-D871-4DFC-84A3-CA60EB52FF0A">D2D1_LAYER_PARAMETERS1</a>*</b>

The parameters that defines the layer.


### -param layer [in, optional]

Type: <b><a href="https://msdn.microsoft.com/ce7b2345-f0e5-4e44-9146-b1f140bb00ca">ID2D1Layer</a>*</b>

The layer resource to push on the device context that receives subsequent drawing operations. 

<div class="alert"><b>Note</b>  If a layer is not specified, Direct2D manages the layer resource automatically.</div>
<div> </div>

## -returns



This method does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/a54dd628-c2a2-4b04-9ced-7749a395f187">ID2D1DeviceContext</a>
 

 

