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

# PCLUSAPI_CLUSTER_GROUP_CLOSE_ENUM_EX callback function


## -description


Closes the enumeration and frees any memory held by the <i>hGroupEnumEx</i> 
    handle. The <b>PCLUSAPI_CLUSTER_GROUP_CLOSE_ENUM_EX</b> type defines a pointer to 
    this function.


## -parameters




### -param hGroupEnumEx [in]

The handle to the enumeration that will be freed.


## -returns



ERROR_SUCCESS is returned when the enumeration handle is freed.




## -remarks



Any additional calls using the <i>hGroupEnumEx</i> will fail.  Do not use the 
    <i>hGroupEnumEx</i> handle after the 
    <i>ClusterGroupCloseEnumEx</i> function is 
    called.



