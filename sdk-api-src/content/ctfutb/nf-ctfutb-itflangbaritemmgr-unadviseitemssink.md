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

# ITfLangBarItemMgr::UnadviseItemsSink


## -description




## -parameters




### -param ulCount [in]

Contains the number of advise sinks to install.


### -param pdwCookie [in]

Pointer to an array of <b>DWORD</b>s that identify the advise sinks to remove. These cookies are obtained when the advise sinks are installed with <a href="https://msdn.microsoft.com/c01d80eb-9156-4fbf-98ff-7f06b145e72f">ITfLangBarItemMgr::AdviseItemSink</a> or <a href="https://msdn.microsoft.com/c0a3e86b-487b-410a-8bba-c2b5126126d2">ITfLangBarItemMgr::AdviseItemsSink</a>. This array must be at least <i>ulCount</i> elements in length.


## -returns



This method has no return values.




## -see-also




<a href="https://msdn.microsoft.com/a7fa257f-e600-4554-8b23-f73323f37e69">ITfLangBarItemMgr</a>



<a href="https://msdn.microsoft.com/c01d80eb-9156-4fbf-98ff-7f06b145e72f">ITfLangBarItemMgr::AdviseItemSink
      </a>



<a href="https://msdn.microsoft.com/c0a3e86b-487b-410a-8bba-c2b5126126d2">
        ITfLangBarItemMgr::AdviseItemsSink
      </a>
 

 

