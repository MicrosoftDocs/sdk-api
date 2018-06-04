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

# IOfflineFilesConnectionInfo::GetConnectState


## -description


Determines whether an item is online or offline and, if offline, why.


## -parameters




### -param pConnectState [out]

Receives an <a href="https://msdn.microsoft.com/48c19b16-6ccb-4580-916d-0d23b69aafcf">OFFLINEFILES_CONNECT_STATE</a> enumeration value that indicates whether the item is online or offline.

<div class="alert"><b>Note</b>  This value sets the Offline Status property value in Windows Explorer.</div>
<div> </div>

### -param pOfflineReason [out]

If the item is offline, this parameter receives an <a href="https://msdn.microsoft.com/0c55b7c6-f39d-4e04-bf16-a102c4b7d4fa">OFFLINEFILES_OFFLINE_REASON</a> enumeration value that indicates why the item is offline.

<div class="alert"><b>Note</b>  This value generates the parenthesized suffix in the Offline Status property value in Windows Explorer when the status is offline.</div>
<div> </div>

## -returns



Returns <b>S_OK</b> if successful, or an error value otherwise.




## -remarks



This method requires that the item have connection state information.  If that information is unavailable at the time of this method call, the method call will initiate the extra query of the cache item to obtain the current connection state.




## -see-also




<a href="https://msdn.microsoft.com/923c5657-67e7-498a-a46b-97d44368cf3b">IOfflineFilesConnectionInfo</a>
 

 

