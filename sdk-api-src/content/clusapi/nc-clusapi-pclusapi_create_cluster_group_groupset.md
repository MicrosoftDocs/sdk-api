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

# PCLUSAPI_CREATE_CLUSTER_GROUP_GROUPSET callback function


## -description


Adds a  groupset to a <a href="https://msdn.microsoft.com/library/windows/hardware/dn922625">cluster</a> and returns a handle to the newly added groupset.


## -parameters




### -param hCluster [in]

A handle to the target cluster.


### -param lpszGroupSetName








#### - groupSetName [in]

Pointer to a null-terminated Unicode string containing the name of the groupset to be added.


## -returns



If the operation succeeds, 
returns a groupset handle.

If the operation fails, 
returns <b>NULL</b>. For more information about the error, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.



