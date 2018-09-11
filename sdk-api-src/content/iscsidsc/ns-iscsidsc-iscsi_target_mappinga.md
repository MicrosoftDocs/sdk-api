---
UID: NS:iscsidsc.ISCSI_TARGET_MAPPINGA
title: ISCSI_TARGET_MAPPINGA
author: windows-sdk-content
description: ISCSI_TARGET_MAPPING.
old-location: iscsidisc\iscsi_target_mapping.htm
tech.root: iSCSIDisc
ms.assetid: bdc27e67-1d64-42cd-adfa-a792012b7142
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*PISCSI_TARGET_MAPPINGA, ISCSI_TARGET_MAPPING, ISCSI_TARGET_MAPPING structure [iSCSI Discovery Library API], ISCSI_TARGET_MAPPINGA, ISCSI_TARGET_MAPPINGW, PISCSI_TARGET_MAPPING, PISCSI_TARGET_MAPPING structure pointer [iSCSI Discovery Library API], iscsidisc.iscsi_target_mapping, iscsidsc/ISCSI_TARGET_MAPPING, iscsidsc/ISCSI_TARGET_MAPPINGA, iscsidsc/ISCSI_TARGET_MAPPINGW, iscsidsc/PISCSI_TARGET_MAPPING"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: iscsidsc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ISCSI_TARGET_MAPPINGW (Unicode) and ISCSI_TARGET_MAPPINGA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Iscsidsc.h
api_name:
 - ISCSI_TARGET_MAPPING
 - ISCSI_TARGET_MAPPINGA
 - ISCSI_TARGET_MAPPINGW
product: Windows
targetos: Windows
req.typenames: ISCSI_TARGET_MAPPINGA, *PISCSI_TARGET_MAPPINGA
req.redist: 
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
 

 

