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

# SetIScsiIKEInfoW function


## -description


The <b>SetIscsiIKEInfo</b> function establishes the IPsec policy and preshared key for the indicated initiator to use when performing iSCSI connections.



## -parameters




### -param InitiatorName [in]

The name of the initiator HBA for which the IPsec policy is established.


### -param InitiatorPortNumber

TBD


### -param AuthInfo [in]

A pointer to a <a href="https://msdn.microsoft.com/d61036f5-a5e8-4c1a-8f99-57fe8e5c5bd0">IKE_AUTHENTICATION_INFORMATION</a> structure that contains the authentication method. Currently, only the IKE_AUTHENTICATION_PRESHARED_KEY_METHOD is supported. 



### -param Persist [in]

If <b>true</b>, this parameter indicates that the preshared key information will be stored in non-volatile memory and will persist across restarts of the computer or the iSCSI initiator service. 


#### - PortNumber [in]

The port on the initiator HBA with which to associate the key. If this parameter contains a value of <b>ISCSI_ALL_INITIATOR_PORTS</b>, all ports on the initiator are associated with the key.


## -returns



Returns ERROR_SUCCESS if the operation succeeds. Otherwise, it returns the appropriate Win32 or iSCSI error code.





## -see-also




<a href="https://msdn.microsoft.com/81576452-47bf-4732-a09f-dd1f9e2689c9">GetIscsiIKEInfo</a>



<a href="https://msdn.microsoft.com/d61036f5-a5e8-4c1a-8f99-57fe8e5c5bd0">IKE_AUTHENTICATION_INFORMATION</a>
 

 

