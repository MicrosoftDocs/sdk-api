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

# RefreshIScsiSendTargetPortalA function


## -description


The <b>RefreshIscsiSendTargetPortal</b> function instructs the iSCSI initiator service to establish a discovery session with the indicated target portal and transmit a <b>SendTargets</b> request to refresh the list of discovered targets for the iSCSI initiator service.


## -parameters




### -param InitiatorInstance [in, optional]

The name of the Host Bus Adapter (HBA) to use for the <b>SendTargets</b> request. If <b>null</b>, the iSCSI initiator service uses any HBA that can reach the indicated target portal is chosen.


### -param InitiatorPortNumber [in]

The port number on the HBA to use for the <b>SendTargets</b> request. If the value is <b>ISCSI_ALL_INITIATOR_PORTS</b>, the initiator HBA will choose the appropriate port based upon current routing information.


### -param Portal [in]

A pointer to a structure of type <a href="https://msdn.microsoft.com/de78c7ec-c2ce-493a-ad29-2ea10e3d7dff">ISCSI_TARGET_PORTAL</a>  indicating the portal to which the iSCSI initiator service sends the <b>SendTargets</b> request to refresh the list of targets.


## -returns



Returns ERROR_SUCCESS if the operation succeeds. Otherwise, it returns the appropriate Win32 or iSCSI error code.





## -see-also




<a href="https://msdn.microsoft.com/de78c7ec-c2ce-493a-ad29-2ea10e3d7dff">ISCSI_TARGET_PORTAL</a>
 

 

