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

# MsiViewClose function


## -description


The 
<b>MsiViewClose</b> function releases the result set for an executed view.


## -parameters




### -param hView [in]

Handle to a view that is set to release.


## -returns



Note that in low memory situations, this function can raise a STATUS_NO_MEMORY exception.




## -remarks



The 
<b>MsiViewClose</b> function must be called before the 
<a href="https://msdn.microsoft.com/12b2373f-425a-4035-bdb4-be1a5469f1d7">MsiViewExecute</a> function is called again on the view, unless all rows of the result set have been obtained with the 
<a href="https://msdn.microsoft.com/1a973a22-ca3a-4980-9b20-d3c5b43fdd19">MsiViewFetch</a> function.




## -see-also




<a href="database_functions.htm">General Database Access Functions</a>
 

 

