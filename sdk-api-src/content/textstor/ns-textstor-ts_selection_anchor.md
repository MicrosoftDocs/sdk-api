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

# TS_SELECTION_ANCHOR structure


## -description



The <b>TS_SELECTION_ANCHOR</b> structure contains anchor-based text selection data.




## -struct-fields




### -field paStart

Contains the start anchor of the selection.


### -field paEnd

Contains the end anchor of the selection.


### -field style

A <a href="https://msdn.microsoft.com/20d0efc2-604f-4ec6-820d-0f87a6d011b0">TS_SELECTIONSTYLE</a> structure that contains additional selection data.


## -see-also




<a href="https://msdn.microsoft.com/df1b21b7-b539-4546-96be-243a8e7ea75a">ITextStoreAnchor::GetSelection
      </a>



<a href="https://msdn.microsoft.com/ce301fa4-d1dd-4470-b8b5-fc944afdc621">
        ITextStoreAnchor::SetSelection
      </a>



<a href="https://msdn.microsoft.com/20d0efc2-604f-4ec6-820d-0f87a6d011b0">
        TS_SELECTIONSTYLE
      </a>
 

 

