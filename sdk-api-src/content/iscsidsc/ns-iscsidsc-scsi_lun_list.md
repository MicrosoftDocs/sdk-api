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

# SCSI_LUN_LIST structure


## -description


The <b>SCSI_LUN_LIST</b> structure is used to construct a list of logical unit numbers (LUNs) associated with target devices.


## -struct-fields




### -field OSLUN

The LUN assigned by the operating system to the target device when it was enumerated by the initiator Host Bus Adapter (HBA).


### -field TargetLUN

The LUN assigned by the target subsystem to the target device.


## -see-also




<a href="https://msdn.microsoft.com/bdc27e67-1d64-42cd-adfa-a792012b7142">ISCSI_TARGET_MAPPING</a>
 

 

