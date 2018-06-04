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

# PeerDistGetStatusEx function


## -description


The <b>PeerDistGetStatusEx</b> function returns the current status and capabilities of the Peer Distribution service.


## -parameters




### -param hPeerDist [in]

A <b>PEERDIST_INSTANCE_HANDLE</b> returned by <a href="https://msdn.microsoft.com/62d4f139-ab18-4d65-bda5-1cf09d7ddab9">PeerDistStartup</a>.


### -param pPeerDistStatus

TBD




#### - pPeerDistStatusInfo [in, out]

A pointer to a <a href="https://msdn.microsoft.com/6EE58EA9-BA0A-4A96-9F9C-EFAF2ABA37C6">PEERDIST_STATUS_INFO</a> structure that contains the current status and capabilities of the Peer Distribution service.


## -returns



If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.




## -remarks



A Group Policy change can result in the Peer Distribution service  moving to an  available, unavailable, or disabled state. Depending on the resultant state of this transition, the content, content information, or stream handles  the caller has access to may  no longer function. If this is the case, the caller must explicitly close the handles by calling the appropriate Peer Distribution API.




## -see-also




<a href="https://msdn.microsoft.com/d693dc1c-39ce-4a2b-b769-9d370abc3d3c">PEERDIST_STATUS</a>



<a href="https://msdn.microsoft.com/6EE58EA9-BA0A-4A96-9F9C-EFAF2ABA37C6">PEERDIST_STATUS_INFO</a>
 

 

