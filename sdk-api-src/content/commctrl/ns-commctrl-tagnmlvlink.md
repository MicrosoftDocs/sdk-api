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

# tagNMLVLINK structure


## -description


Contains information about an <a href="https://msdn.microsoft.com/de8f40d6-b79e-4324-af67-9a3c0915609d">LVN_LINKCLICK</a> notification code.



## -struct-fields




### -field hdr

Type: <b><a href="https://msdn.microsoft.com/0c8b116b-82ad-495a-b19d-8c172e0b2608">NMHDR</a></b>


<a href="https://msdn.microsoft.com/0c8b116b-82ad-495a-b19d-8c172e0b2608">NMHDR</a> structure that contains basic information about the notification code.


### -field link

Type: <b><a href="https://msdn.microsoft.com/c3d62876-b92a-43b0-bc23-8b006847a474">LITEM</a></b>


<a href="https://msdn.microsoft.com/c3d62876-b92a-43b0-bc23-8b006847a474">LITEM</a> structure that contains information about the link that was clicked.


### -field iItem

Type: <b>int</b>

Index of the item that contains the link.


### -field iSubItem

Type: <b>int</b>

Subitem, if any. This member may be <b>NULL</b>. For a link in a group header, this is the group identifier, as set in <a href="https://msdn.microsoft.com/512a8524-d5f9-47c0-a28e-47c3c1a713bf">LVGROUP</a>.

