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

# IExtractImage::Extract


## -description


Requests an image from an object, such as an item in a Shell folder.


## -parameters




### -param phBmpThumbnail






#### - phBmpImage [out]

Type: <b>HBITMAP*</b>

The buffer to hold the bitmapped image.


## -returns



Type: <b>HRESULT</b>

Returns S_OK if successful, or a COM-defined error code otherwise.




## -remarks



You must call <a href="https://msdn.microsoft.com/f1113429-ea89-4650-b345-db9e275232e6">IExtractImage::GetLocation</a> prior to calling <b>Extract</b>.



