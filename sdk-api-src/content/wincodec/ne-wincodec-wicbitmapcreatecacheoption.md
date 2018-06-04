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

# WICBitmapCreateCacheOption enumeration


## -description


Specifies the desired cache usage.


## -enum-fields




### -field WICBitmapNoCache

Do not cache the bitmap.


### -field WICBitmapCacheOnDemand

Cache the bitmap when needed.


### -field WICBitmapCacheOnLoad

Cache the bitmap at initialization.


### -field WICBITMAPCREATECACHEOPTION_FORCE_DWORD




## -remarks



The <b>CreateBitmap</b> of the <a href="https://msdn.microsoft.com/30d155b1-a46c-46c4-9f8f-fb56dc6bf0a9">IWICImagingFactory</a> interface does not support WICBitmapNoCache when the <i>pixelFormat</i> is a native pixel format provided by Windows Imaging Component (WIC).



