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

# RemoveIScsiPersistentTargetA function


## -description


The <b>RemoveIscsiPersistentTarget</b> function removes a persistent login for the specified hardware initiator Host Bus Adapter (HBA), initiator port, and target portal.


## -parameters




### -param InitiatorInstance [in]

The name of the initiator that maintains the persistent login to remove. 


### -param InitiatorPortNumber [in, optional]

The port number on which the initiator connects to <i>TargetName</i>. If <i>InitiatorPortNumber</i> is <b>ISCSI_ALL_INITIATOR_PORTS</b> the miniport driver for the initiator HBA removes the <i>TargetName</i> from the persistent login lists for all initiator ports. 



### -param TargetName [in]

The name of the target.


### -param Portal [in]

The portal through which the initiator connects to the target. If <i>Portal</i> is <b>null</b> or contains no information, the miniport driver for the initiator HBA removes persistent logins for the target on all portals. 


## -returns



Returns ERROR_SUCCESS if the operation succeeds. Otherwise, it returns the appropriate Win32 or iSCSI error code.





## -see-also




<a href="https://msdn.microsoft.com/184b256b-0cb0-45c1-8f73-5ff28fb388fb">AddPersistentIscsiDevice</a>



<a href="https://msdn.microsoft.com/9e21dde6-face-40ae-803b-2aa7861e6f4f">ClearPersistentIscsiDevices</a>



<a href="https://msdn.microsoft.com/4016d8e4-de67-4c49-b54f-31c1b7bd64a8">RemovePersistentIscsiDevice</a>



<a href="https://msdn.microsoft.com/0ab1a864-b44e-4307-9f7c-93cc0d40ff3a">ReportIscsiPersistentLogins</a>



<a href="https://msdn.microsoft.com/856e240d-8c4d-4e55-aef3-71f98193c221">ReportPersistentIscsiDevices</a>



<a href="https://msdn.microsoft.com/b21e5872-24b2-4a4c-86a7-528789c1b9aa">SetupPersistentIscsiDevices</a>
 

 

