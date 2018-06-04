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

# IWTSPluginServiceProvider::GetService


## -description


Obtains the specified service.


## -parameters




### -param ServiceId [in]

Specifies the service to retrieve. This can be the following values.



#### RDCLIENT_BITMAP_RENDER_SERVICE

Identifies the bitmap rendering service. The <i>ppunkObject</i> parameter receives an <a href="https://msdn.microsoft.com/5ddc6ad8-1006-473e-b0f4-a5829045219a">IWTSBitmapRenderService</a> interface pointer.


### -param ppunkObject [out]

The address of a pointer to an <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface that receives the service object.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/8baf8d8b-95a0-46bd-81ea-e99a7db45cdc">IWTSPluginServiceProvider</a>
 

 

