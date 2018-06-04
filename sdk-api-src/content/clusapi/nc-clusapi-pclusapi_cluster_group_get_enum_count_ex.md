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

# PCLUSAPI_CLUSTER_GROUP_GET_ENUM_COUNT_EX callback function


## -description


Returns the number of elements in the enumeration.
   The <b>PCLUSAPI_CLUSTER_GROUP_GET_ENUM_COUNT_EX</b> type defines a pointer to this function.


## -parameters




### -param hGroupEnumEx [in]

The handle to the enumeration from which the number of entries will be returned.


## -returns



The number of items in the enumeration.




## -remarks



The <i>ClusterGroupGetEnumCountEx</i> function doesn't connect to the cluster, because <i>hGroupEnumEx</i> handle already contains the enumeration data.



