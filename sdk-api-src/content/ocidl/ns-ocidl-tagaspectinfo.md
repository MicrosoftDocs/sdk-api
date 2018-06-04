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

# tagAspectInfo structure


## -description


Contains information that is used by the <a href="https://msdn.microsoft.com/913593ff-07fe-44bd-88dc-8e58da82089b">IViewObject::Draw</a> method to optimize rendering of an inactive object by making more efficient use of the GDI.


## -struct-fields




### -field cb

The size of the structure, in bytes.


### -field dwFlags

A value taken from the <a href="https://msdn.microsoft.com/639871a6-85ab-41e2-92fa-7f1e72e9cb38">DVASPECTINFOFLAG</a> enumeration.



## -see-also




<a href="https://msdn.microsoft.com/639871a6-85ab-41e2-92fa-7f1e72e9cb38">DVASPECTINFOFLAG</a>



<a href="https://msdn.microsoft.com/913593ff-07fe-44bd-88dc-8e58da82089b">IViewObject::Draw</a>
 

 

