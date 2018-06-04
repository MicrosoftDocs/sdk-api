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

# tagNMTVSTATEIMAGECHANGING structure


## -description


Contains information about an <a href="https://msdn.microsoft.com/8e42d8b3-5e76-4d03-94b0-3e4583669095">NM_TVSTATEIMAGECHANGING</a> notification code.


## -struct-fields




### -field hdr

Type: <b><a href="https://msdn.microsoft.com/0c8b116b-82ad-495a-b19d-8c172e0b2608">NMHDR</a></b>


<a href="https://msdn.microsoft.com/0c8b116b-82ad-495a-b19d-8c172e0b2608">NMHDR</a> structure that contains information about this notification code.


### -field hti

Type: <b>HTREEITEM</b>

Handle to the tree-view item whose state image is changing.


### -field iOldStateImageIndex

Type: <b>int</b>

The index of the old state image.


### -field iNewStateImageIndex

Type: <b>int</b>

The index of the new state image.

