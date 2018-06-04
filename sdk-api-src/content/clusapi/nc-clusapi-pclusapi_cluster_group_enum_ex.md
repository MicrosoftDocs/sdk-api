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

# PCLUSAPI_CLUSTER_GROUP_ENUM_EX callback function


## -description


Retrieves an item in the enumeration.
   The <b>PCLUSAPI_CLUSTER_GROUP_ENUM_EX</b> type defines a pointer to this function.


## -parameters




### -param hGroupEnumEx [in]

The handle to the enumeration from which the item will be retrieved.


### -param dwIndex [in]

The zero-based index of the item in the enumeration.


### -param pItem [in, out]

A pointer to the buffer to be filled.


### -param cbItem [in, out]

On input, the size of <i>pItem</i>.

On output, either the required size in bytes of the buffer if the buffer is too small, or the number of bytes written into the buffer.


## -returns





Returns DWORD that ...






## -remarks



The <i>ClusterGroupEnumEx</i> function doesn't connect to the cluster, because the <i>hGroupEnumEx</i> already contains the enumeration data.  The data is copied into the buffer but no data is retrieved from the cluster.



