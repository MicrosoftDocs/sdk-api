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

# _reqresize structure


## -description


Contains the requested size of a rich edit control. A rich edit control sends this structure to its parent window as part of an <a href="https://msdn.microsoft.com/708c23b1-7b81-46f1-9595-46230693855d">EN_REQUESTRESIZE</a> notification code.


## -struct-fields




### -field nmhdr

Type: <b><a href="https://msdn.microsoft.com/0c8b116b-82ad-495a-b19d-8c172e0b2608">NMHDR</a></b>

Notification header. 


### -field rc

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a></b>

Requested new size. 


## -see-also




<a href="https://msdn.microsoft.com/708c23b1-7b81-46f1-9595-46230693855d">EN_REQUESTRESIZE</a>
 

 

