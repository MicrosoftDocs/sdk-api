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

# _DWM_THUMBNAIL_PROPERTIES structure


## -description


Specifies Desktop Window Manager (DWM) thumbnail properties. Used by the <a href="https://msdn.microsoft.com/02c40cda-b87c-44c5-bcc5-3d0e83b7b14b">DwmUpdateThumbnailProperties</a> function.


## -struct-fields




### -field dwFlags

A bitwise combination of <a href="https://msdn.microsoft.com/8eee1baf-e24e-40af-92ab-a7acae267ecc">DWM thumbnail constant</a> values that indicates which members of this structure are set.


### -field rcDestination

The area in the destination window where the thumbnail will be rendered.


### -field rcSource

The region of the source window to use as the thumbnail. By default, the entire window is used as the thumbnail.


### -field opacity

The opacity with which to render the thumbnail. 0 is fully transparent while 255 is fully opaque. The default value is 255.


### -field fVisible

<b>TRUE</b> to make the thumbnail visible; otherwise, <b>FALSE</b>. The default is <b>FALSE</b>.


### -field fSourceClientAreaOnly

<b>TRUE</b> to use only the thumbnail source's client area; otherwise, <b>FALSE</b>. The default is <b>FALSE</b>.

