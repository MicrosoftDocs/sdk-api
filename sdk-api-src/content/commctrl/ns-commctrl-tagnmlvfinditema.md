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

# tagNMLVFINDITEMA structure


## -description


Contains information the owner needs to find items requested by a <a href="List_View_Controls_Overview.htm">virtual list-view</a> control. This structure is used with the <a href="https://msdn.microsoft.com/5a3f9fed-0c57-46bf-b986-ea8b54290b5e">LVN_ODFINDITEM</a> notification code. 


## -struct-fields




### -field hdr

Type: <b><a href="https://msdn.microsoft.com/0c8b116b-82ad-495a-b19d-8c172e0b2608">NMHDR</a></b>


<a href="https://msdn.microsoft.com/0c8b116b-82ad-495a-b19d-8c172e0b2608">NMHDR</a> structure that contains information on this notification code. 


### -field iStart

Type: <b>int</b>

Index of the item at which the search will start. 


### -field lvfi

Type: <b><a href="https://msdn.microsoft.com/6d78c0ec-9735-407d-a20b-efb7dc3b0fba">LVFINDINFO</a></b>


<a href="https://msdn.microsoft.com/6d78c0ec-9735-407d-a20b-efb7dc3b0fba">LVFINDINFO</a> structure that contains information necessary to perform a search. 

