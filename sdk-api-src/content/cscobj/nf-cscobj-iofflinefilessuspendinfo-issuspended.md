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

# IOfflineFilesSuspendInfo::IsSuspended


## -description


Determines whether an item is suspended.

If an item is suspended and is a suspended root, it was suspended by using the <a href="https://msdn.microsoft.com/5307bc8c-e6e9-4ae7-b2da-036fc9c5c08d">IOfflineFilesSuspend::SuspendRoot</a> method.  If an item is suspended but is not a suspended root, its suspension was inherited from a suspended root.


## -parameters




### -param pbSuspended [out]

Receives <b>TRUE</b> if the item is suspended, or <b>FALSE</b> otherwise.


### -param pbSuspendedRoot [out]

Receives <b>TRUE</b> if the item is a suspended root, or <b>FALSE</b> otherwise.  If the item is not suspended, this value is always <b>FALSE</b>.


## -returns



Returns <b>S_OK</b> if successful, or an error value otherwise.




## -see-also




<a href="https://msdn.microsoft.com/b9f9e30e-df37-467e-ac59-7955e0eae3c0">IOfflineFilesSuspendInfo</a>
 

 

