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

# ISCSI_SESSION_INFOW structure


## -description


The <b>ISCSI_SESSION_INFO</b> structure contains session information.


## -struct-fields




### -field SessionId

A <a href="https://msdn.microsoft.com/d13975f9-58d0-425c-a2de-a0d1d70850d3">ISCSI_UNIQUE_SESSION_ID</a> structure containing a unique identifier that represents the session.


### -field InitiatorName

A string that represents the initiator name.


### -field TargetNodeName

A string that represents the target node name.


### -field TargetName

A string that represents the target name.


### -field ISID

The initiator-side identifier (ISID) used in the iSCSI protocol.


### -field TSID

The target-side identifier (TSID) used in the iSCSI protocol.


### -field ConnectionCount

The number of connections associated with the session.


### -field Connections

A pointer to a <a href="https://msdn.microsoft.com/4bfe2f36-2e68-4093-9660-b0140baeea80">ISCSI_CONNECTION_INFO</a> structure.


## -see-also




<a href="https://msdn.microsoft.com/b16b9e52-67af-4745-ac67-a2096dafe94e">GetIScsiSessionList</a>



<a href="https://msdn.microsoft.com/4bfe2f36-2e68-4093-9660-b0140baeea80">ISCSI_CONNECTION_INFO</a>



<a href="https://msdn.microsoft.com/d13975f9-58d0-425c-a2de-a0d1d70850d3">ISCSI_UNIQUE_SESSION_ID</a>
 

 

