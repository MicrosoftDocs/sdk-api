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

# IFsrmFileScreenException::get_Path


## -description


<p class="CCE_Message">[This property is supported for compatibility but it's recommended to use the 
    <a href="https://msdn.microsoft.com/1CE772FA-CE33-4900-A499-058175A7C37E">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="https://msdn.microsoft.com/1787aab2-b315-418c-81bf-1e42198c8780">MSFT_FSRMFileScreenException</a> class.]

Retrieves the path that is associated with this file screen exception.

This property is read-only.


## -parameters


## -remarks



Note that if the path is renamed, the exception becomes associated with the new path. If the path is deleted, 
    the exception is deleted.




## -see-also




<a href="https://msdn.microsoft.com/188e76dd-6df6-412f-8d51-fc727075de80">IFsrmFileScreenException</a>



<a href="https://msdn.microsoft.com/1787aab2-b315-418c-81bf-1e42198c8780">MSFT_FSRMFileScreenException</a>
 

 

