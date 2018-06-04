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

# _ITEMSPACING structure


## -description


Stores the dimensions of the two possible sizes of icon spacing that are available for display: small and large. Used by <a href="https://msdn.microsoft.com/92450bc7-26e5-4061-90f7-eea0f0a4db09">IShellFolderView::GetItemSpacing</a>.


## -struct-fields




### -field cxSmall

Type: <b>int</b>

The width of the spacing between icons in small icon mode, in pixels.


### -field cySmall

Type: <b>int</b>

The height of the spacing between icons in small icon mode, in pixels.


### -field cxLarge

Type: <b>int</b>

The width of the spacing between icons in large icon mode, in pixels.


### -field cyLarge

Type: <b>int</b>

The height of the spacing between icons in large icon mode, in pixels.

