---
UID: NS:iscsidsc.__unnamed_struct_17
title: ISCSI_SESSION_INFOA
author: windows-sdk-content
description: ISCSI_SESSION_INFO.
old-location: iscsidisc\iscsi_session_info.htm
tech.root: iSCSIDisc
ms.assetid: 5da4aa28-a630-41f2-abb2-5538c11242e6
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PISCSI_SESSION_INFOA, ISCSI_SESSION_INFO, ISCSI_SESSION_INFO structure [iSCSI Discovery Library API], ISCSI_SESSION_INFOA, ISCSI_SESSION_INFOW, PISCSI_SESSION_INFO, PISCSI_SESSION_INFO structure pointer [iSCSI Discovery Library API], iscsidisc.iscsi_session_info, iscsidsc/ISCSI_SESSION_INFO, iscsidsc/ISCSI_SESSION_INFOA, iscsidsc/ISCSI_SESSION_INFOW, iscsidsc/PISCSI_SESSION_INFO"
ms.topic: struct
req.header: iscsidsc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ISCSI_SESSION_INFOW (Unicode) and ISCSI_SESSION_INFOA (ANSI)
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
 - ISCSI_SESSION_INFO
 - ISCSI_SESSION_INFOA
 - ISCSI_SESSION_INFOW
product: Windows
targetos: Windows
req.typenames: ISCSI_SESSION_INFOA, *PISCSI_SESSION_INFOA
req.redist: 
---

# ISCSI_SESSION_INFOA structure


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

A pointer to a <a href="https://msdn.microsoft.com/en-us/library/Bb870793(v=VS.85).aspx">ISCSI_CONNECTION_INFO</a> structure.


## -see-also




<a href="https://msdn.microsoft.com/b16b9e52-67af-4745-ac67-a2096dafe94e">GetIScsiSessionList</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb870793(v=VS.85).aspx">ISCSI_CONNECTION_INFO</a>



<a href="https://msdn.microsoft.com/d13975f9-58d0-425c-a2de-a0d1d70850d3">ISCSI_UNIQUE_SESSION_ID</a>
 

 

