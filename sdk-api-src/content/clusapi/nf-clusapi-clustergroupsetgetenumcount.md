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

# ClusterGroupSetGetEnumCount function


## -description


Gets the number of items contained  the enumerator's collection.


## -parameters




### -param hGroupSetEnum [in]

A handle to an enumerator returned by <a href="https://msdn.microsoft.com/9e629cc8-2e5f-4682-a9b5-902d13a9792d">ClusterGroupSetOpenEnum</a>.


## -returns



The number of items in the enumerator's collection. May be zero.



