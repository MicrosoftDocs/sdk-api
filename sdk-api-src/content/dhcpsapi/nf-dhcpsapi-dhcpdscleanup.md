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

# DhcpDsCleanup function


## -description



      The <b>DhcpDsCleanup</b> function frees up directory service resources allocated for DHCP services by <a href="https://msdn.microsoft.com/c622d492-91a8-4fd3-87ed-3545e7b83a0a">DhcpDsInit</a>. This function should be called exactly once for each corresponding DHCP service process, and only when the process is terminated. 


## -parameters






## -returns



This function has no return values.




## -see-also




<a href="https://msdn.microsoft.com/c622d492-91a8-4fd3-87ed-3545e7b83a0a">DhcpDsInit</a>
 

 

