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

# TTIsEmbeddingEnabledForFacename function


## -description


Determines whether embedding is enabled for a specified font.


## -parameters




### -param lpszFacename [in]

Pointer to the facename of the font, such as Arial Bold.


### -param pbEnabled [out]

Pointer to a boolean, set upon completion of the function. A nonzero value indicates the font is not in the typeface exclusion list, and, therefore, can be embedded without conflict.


## -returns



If successful, returns E_NONE.

<i>pbEnabled</i> is filled with a boolean that indicates whether embedding is currently enabled within a device context for the specified font.

Otherwise, returns an error code described in <a href="https://msdn.microsoft.com/71effafe-55a9-40ed-81c7-07278eba32d3">Embedding-Function Error Messages</a>.




## -remarks



If successful, the client may embed the font.

For additional information on the exclusion list, see the Remarks section of <a href="https://msdn.microsoft.com/05d74bfb-28c4-4e1a-9e18-df868f8fa784">TTEnableEmbeddingForFacename</a>.




## -see-also




<a href="https://msdn.microsoft.com/05d74bfb-28c4-4e1a-9e18-df868f8fa784">TTEnableEmbeddingForFacename</a>



<a href="https://msdn.microsoft.com/0ce9ade0-df5b-4a2a-adf6-ca641e27d2bd">TTGetEmbeddedFontInfo</a>



<a href="https://msdn.microsoft.com/c442447f-221d-4bce-9749-fb9fbe333808">TTGetEmbeddingType</a>



<a href="https://msdn.microsoft.com/f1e3112b-d840-45eb-bb99-416319ed9e15">TTIsEmbeddingEnabled</a>
 

 

