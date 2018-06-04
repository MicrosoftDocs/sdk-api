---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# IWICBitmapScaler::Initialize


## -description


Initializes the bitmap scaler with the provided parameters.


## -parameters




### -param pISource [in]

Type: <b><a href="https://msdn.microsoft.com/abcc84af-6067-4856-8618-fb66aff4255a">IWICBitmapSource</a>*</b>

The input bitmap source.


### -param uiWidth [in]

Type: <b>UINT</b>

The destination width.


### -param uiHeight [in]

Type: <b>UINT</b>

The desination height.


### -param mode [in]

Type: <b><a href="https://msdn.microsoft.com/7c707ab7-7cd5-418f-921c-e9114da92f2a">WICBitmapInterpolationMode</a></b>

The <a href="https://msdn.microsoft.com/7c707ab7-7cd5-418f-921c-e9114da92f2a">WICBitmapInterpolationMode</a> to use when scaling.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks




<a href="https://msdn.microsoft.com/cc14be9d-d750-40db-a95f-309b392cefe8">IWICBitmapScaler</a> can't be initialized multiple times. For example, when scaling every frame in a multi-frame image, a new <b>IWICBitmapScaler</b> must be created and initialized for each frame.


#### Examples

For an example using an <a href="https://msdn.microsoft.com/cc14be9d-d750-40db-a95f-309b392cefe8">IWICBitmapScaler</a>, see the <a href="https://msdn.microsoft.com/d2c65c9b-6f52-46f7-935d-0c582ca83867">How to Scale a Bitmap Source</a> topic.

<div class="code"></div>


