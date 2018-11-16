---
UID: NE:d2d1_1.D2D1_LAYER_OPTIONS1
title: D2D1_LAYER_OPTIONS1
author: windows-sdk-content
description: Specifies how the layer contents should be prepared.
old-location: direct2d\d2d1_layer_options1.htm
tech.root: Direct2D
ms.assetid: 13C9EDE7-A1D0-4359-8EF3-77FF763B9244
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: D2D1_LAYER_OPTIONS1, D2D1_LAYER_OPTIONS1 enumeration [Direct2D], D2D1_LAYER_OPTIONS1_IGNORE_ALPHA, D2D1_LAYER_OPTIONS1_INITIALIZE_FROM_BACKGROUND, D2D1_LAYER_OPTIONS1_NONE, d2d1_1/D2D1_LAYER_OPTIONS1, d2d1_1/D2D1_LAYER_OPTIONS1_IGNORE_ALPHA, d2d1_1/D2D1_LAYER_OPTIONS1_INITIALIZE_FROM_BACKGROUND, d2d1_1/D2D1_LAYER_OPTIONS1_NONE, direct2d.d2d1_layer_options1
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: d2d1_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d2d1_1.h
api_name:
 - D2D1_LAYER_OPTIONS1
product: Windows
targetos: Windows
req.typenames: D2D1_LAYER_OPTIONS1
req.redist: 
---

# D2D1_LAYER_OPTIONS1 enumeration


## -description


Specifies how the layer contents should be prepared.



## -enum-fields




### -field D2D1_LAYER_OPTIONS1_NONE

Default layer behavior. A premultiplied layer target is pushed and its contents are cleared to transparent black. 



### -field D2D1_LAYER_OPTIONS1_INITIALIZE_FROM_BACKGROUND

	The layer is not cleared to transparent black.


### -field D2D1_LAYER_OPTIONS1_IGNORE_ALPHA

	The layer is always created as ignore alpha. All content rendered into the layer will be treated as opaque.


### -field D2D1_LAYER_OPTIONS1_FORCE_DWORD



