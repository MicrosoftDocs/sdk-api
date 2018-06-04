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

# IUpdateSearcher::get_ServerSelection


## -description


Gets and sets a <a href="https://msdn.microsoft.com/51caac5e-98a6-49e4-a175-6319349a6d68">ServerSelection</a> value that indicates the server to search for updates.

This property is read/write.


## -parameters


## -remarks



 The site that is not a Windows Update site that is specified by the value of the <a href="https://msdn.microsoft.com/7c00d26a-9ef0-45ec-81b3-d13f91dd7d8d">ServiceID</a> property is searched only if the value of the <b>ServerSelection</b> property is  ssOthers.




## -see-also




<a href="https://msdn.microsoft.com/f41b1689-d9fe-4697-91e9-a176d3b592c7">IUpdateSearcher</a>
 

 

