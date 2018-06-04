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

# ITaskSettings::put_NetworkSettings


## -description


Gets or sets the network settings object that contains a network profile identifier and name. If the <a href="https://msdn.microsoft.com/d0926d75-e7d9-469c-aaa0-ddee8fe22dcd">RunOnlyIfNetworkAvailable</a> property of <a href="https://msdn.microsoft.com/203264d1-f67c-45ba-931b-206d7f57a2a6">ITaskSettings</a> is  <b>true</b> and a network propfile is specified in the <b>NetworkSettings</b> property, then the task will run only if the specified network profile is available.

This property is read/write.


## -parameters


## -see-also




<a href="https://msdn.microsoft.com/831e1259-df2b-4b03-8336-706727fd7b14">INetworkSettings</a>



<a href="https://msdn.microsoft.com/203264d1-f67c-45ba-931b-206d7f57a2a6">ITaskSettings</a>
 

 

