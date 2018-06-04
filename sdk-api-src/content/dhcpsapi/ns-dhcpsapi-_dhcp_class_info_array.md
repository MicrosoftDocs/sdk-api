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

# _DHCP_CLASS_INFO_ARRAY structure


## -description


The <b>DHCP_CLASS_INFO_ARRAY</b> structure defines an array of elements that contain DHCP class information.


## -struct-fields




### -field NumElements

Specifies the number of elements in <b>Classes</b>.


### -field Classes

Pointer to an array of <a href="https://msdn.microsoft.com/62fb9f21-ad21-4525-90f4-48dc5a8b230b">DHCP_CLASS_INFO</a> structures that contain DHCP class information.


### -field Classes.size_is

 


### -field Classes.size_is.NumElements

 




## -see-also




<a href="https://msdn.microsoft.com/62fb9f21-ad21-4525-90f4-48dc5a8b230b">DHCP_CLASS_INFO</a>



<a href="https://msdn.microsoft.com/93f37424-1a81-477e-85da-359885e94349">DhcpEnumClasses</a>
 

 

