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

# ISCSI_TARGET_MAPPINGA structure


## -description


The 		ISCSI_TARGET_MAPPING structure contains information about a target and the Host-Bus  Adapters (HBAs) and buses through which the target is reached.


## -struct-fields




### -field InitiatorName

A string representing the name of the HBA initiator through which the target is accessed.


### -field TargetName

A string representing the target name.


### -field OSDeviceName

A string representing the device name of the HBA initiator; for example '<b>\device\ScsiPort3</b>'. 


### -field SessionId

A <a href="https://msdn.microsoft.com/d13975f9-58d0-425c-a2de-a0d1d70850d3">ISCSI_UNIQUE_SESSION_ID</a> structure containing information that uniquely identifies the session..


### -field OSBusNumber

The bus number used by the initiator as the local SCSI address of the target.


### -field OSTargetNumber

The target number used by the initiator as the local SCSI address of the target.


### -field LUNCount

The number of logical units (LUN) on the target.


### -field LUNList

A list of SCSI_LUN_LIST structures that contain information about the LUNs associated with the target.


### -field LUNList.size_is

 


### -field LUNList.size_is.LUNCount

 




## -see-also




<a href="https://msdn.microsoft.com/d13975f9-58d0-425c-a2de-a0d1d70850d3">ISCSI_UNIQUE_SESSION_ID</a>
 

 

