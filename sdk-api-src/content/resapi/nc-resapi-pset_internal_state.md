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

# PSET_INTERNAL_STATE callback function


## -description


Sets the internal state of a resource


## -parameters




### -param Arg1


### -param stateType [in]

A <a href="https://msdn.microsoft.com/A67B8251-214B-44DD-8166-C0F74335CE1F">CLUSTER_RESOURCE_APPLICATION_STATE</a> value


### -param active [in]

Whether the resource is active


#### - [in]

A resource handle

