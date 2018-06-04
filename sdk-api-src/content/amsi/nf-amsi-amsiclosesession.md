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

# AmsiCloseSession function


## -description


Close a session that was opened by <a href="https://msdn.microsoft.com/588C9003-8689-4D1C-BDFB-386E60BAECD5">AmsiOpenSession</a>.


## -parameters




### -param amsiContext [in]

The handle of type HAMSICONTEXT that was initially received from <a href="https://msdn.microsoft.com/946FC79C-556C-404E-A559-323AA69B3EC6">AmsiInitialize</a>.


### -param amsiSession

TBD




#### - session [in]

The handle of type HAMSISESSION that was initially received from <a href="https://msdn.microsoft.com/588C9003-8689-4D1C-BDFB-386E60BAECD5">AmsiOpenSession</a>.


## -returns



This function does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/946FC79C-556C-404E-A559-323AA69B3EC6">AmsiInitialize</a>



<a href="https://msdn.microsoft.com/588C9003-8689-4D1C-BDFB-386E60BAECD5">AmsiOpenSession</a>
 

 

