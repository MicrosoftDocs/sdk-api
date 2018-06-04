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

# tagNMLINK structure


## -description


The <b>NMLINK</b> Contains notification information. Send this structure with the <a href="https://msdn.microsoft.com/e92d7c92-f2c6-44aa-bce5-3bb07c184e7d">NM_CLICK</a> or <a href="https://msdn.microsoft.com/2c4839bc-6b23-469b-978f-cdf5f7bc0549">NM_RETURN</a> messages.


## -struct-fields




### -field hdr

Type: <b><a href="https://msdn.microsoft.com/0c8b116b-82ad-495a-b19d-8c172e0b2608">NMHDR</a></b>


<a href="https://msdn.microsoft.com/0c8b116b-82ad-495a-b19d-8c172e0b2608">NMHDR</a> structure that contains information about the notification.


### -field item

Type: <b><a href="https://msdn.microsoft.com/c3d62876-b92a-43b0-bc23-8b006847a474">LITEM</a></b>


<a href="https://msdn.microsoft.com/c3d62876-b92a-43b0-bc23-8b006847a474">LITEM</a> structure that contains information about the link item.


## -see-also




<a href="https://msdn.microsoft.com/c3d62876-b92a-43b0-bc23-8b006847a474">LITEM</a>



<a href="https://msdn.microsoft.com/0c8b116b-82ad-495a-b19d-8c172e0b2608">NMHDR</a>



<a href="https://msdn.microsoft.com/e92d7c92-f2c6-44aa-bce5-3bb07c184e7d">NM_CLICK (syslink)</a>



<b>Reference</b>
 

 

