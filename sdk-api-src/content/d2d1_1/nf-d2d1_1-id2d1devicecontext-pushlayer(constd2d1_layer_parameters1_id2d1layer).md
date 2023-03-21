---
UID: NF:d2d1_1.ID2D1DeviceContext.PushLayer(constD2D1_LAYER_PARAMETERS1,ID2D1Layer)
title: ID2D1DeviceContext::PushLayer (d2d1_1.h)
description: Push a layer onto the clip and layer stack of the device context. (overload 1/2)
helpviewer_keywords: ["ID2D1DeviceContext interface [Direct2D]","PushLayer method","ID2D1DeviceContext.PushLayer","ID2D1DeviceContext::PushLayer","PushLayer","PushLayer method [Direct2D]","PushLayer method [Direct2D]","ID2D1DeviceContext interface","d2d1_1/ID2D1DeviceContext::PushLayer","direct2d.id2d1devicecontext_pushlayer"]
old-location: direct2d\id2d1devicecontext_pushlayer.htm
tech.root: Direct2D
ms.assetid: 7DC719E3-CE94-4B7F-B02D-62D78425CFFE
ms.date: 12/05/2018
ms.keywords: ID2D1DeviceContext interface [Direct2D],PushLayer method, ID2D1DeviceContext.PushLayer, ID2D1DeviceContext::PushLayer, PushLayer, PushLayer method [Direct2D], PushLayer method [Direct2D],ID2D1DeviceContext interface, d2d1_1/ID2D1DeviceContext::PushLayer, direct2d.id2d1devicecontext_pushlayer
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID2D1DeviceContext::PushLayer
 - d2d1_1/ID2D1DeviceContext::PushLayer
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2d1.dll
api_name:
 - ID2D1DeviceContext.PushLayer
---

# ID2D1DeviceContext::PushLayer


## -description

Push a layer onto the clip and layer stack of the device context.

## -parameters

### -param layerParameters [in]

Type: <b>const <a href="/windows/desktop/api/d2d1_1/ns-d2d1_1-d2d1_layer_parameters1">D2D1_LAYER_PARAMETERS1</a>*</b>

The parameters that defines the layer.

### -param layer [in, optional]

Type: <b><a href="/windows/desktop/api/d2d1/nn-d2d1-id2d1layer">ID2D1Layer</a>*</b>

The layer resource to push on the device context that receives subsequent drawing operations. 

<div class="alert"><b>Note</b>  If a layer is not specified, Direct2D manages the layer resource automatically.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1devicecontext">ID2D1DeviceContext</a>
