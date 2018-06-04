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

# RemoveIScsiSendTargetPortalW function


## -description


The <b>RemoveIscsiSendTargetPortal</b> function removes a portal from the list of portals to which the iSCSI initiator service sends <b>SendTargets</b> requests for target discovery.


## -parameters




### -param InitiatorInstance [in, optional]

The name of the Host Bus Adapter (HBA) that the iSCSI initiator service uses to establish a discovery session and perform <b>SendTargets</b> requests. A value of <b>null</b> indicates that the iSCSI initiator service will use any HBA that is capable of accessing the target portal. 



### -param InitiatorPortNumber [in, optional]

The port number on the HBA that the iSCSI initiator service use to perform <b>SendTargets</b> requests. 



### -param Portal [in]

A pointer to a structure of type <a href="https://msdn.microsoft.com/de78c7ec-c2ce-493a-ad29-2ea10e3d7dff">ISCSI_TARGET_PORTAL</a> that specifies the target portal that the iSCSI initiator service removes from its list of portals. 



## -returns



Returns ERROR_SUCCESS if the operation succeeds. Otherwise, it returns the appropriate Win32 or iSCSI error code.





## -see-also




<a href="https://msdn.microsoft.com/de78c7ec-c2ce-493a-ad29-2ea10e3d7dff">ISCSI_TARGET_PORTAL</a>
 

 

