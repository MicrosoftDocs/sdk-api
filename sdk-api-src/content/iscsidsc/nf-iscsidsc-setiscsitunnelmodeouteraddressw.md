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

# SetIScsiTunnelModeOuterAddressW function


## -description


<b>SetIscsiTunnelModeOuterAddress</b> function establishes the tunnel-mode outer address that the indicated initiator Host Bus Adapter (HBA) uses when communicating in IPsec tunnel mode through the specified port.



## -parameters




### -param InitiatorName [in, optional]

The name of the initiator with which the tunnel-mode outer address will be associated. If this parameter is <b>null</b>, all HBA initiators are configured to use the indicated tunnel-mode outer address.


### -param InitiatorPortNumber [in]

Indicates the number of the port with which the tunnel-mode outer address is associated. If this parameter contains <b>ISCSI_ALL_PORTS</b>, all ports on the indicated initiator are associated with the tunnel-mode outer address. 



### -param DestinationAddress [in]

The destination address to associate with the tunnel-mode outer address indicated by <i>OuterModeAddress</i>. 



### -param OuterModeAddress [in]

The tunnel-mode outer address to associate with indicated initiators and ports. 



### -param Persist [in]

When <b>true</b>, this parameter indicates that the iSCSI initiator service stores the tunnel-mode outer address in non-volatile memory and that the address will persist across restarts of the initiator and the iSCSI initiator service. 



## -returns



Returns ERROR_SUCCESS if the operation succeeds.Otherwise, it returns the appropriate Win32 or iSCSI error code.




