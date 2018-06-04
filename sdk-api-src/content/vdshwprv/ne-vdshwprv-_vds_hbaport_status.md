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

# _VDS_HBAPORT_STATUS enumeration


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Defines 
   the set of valid statuses for an HBA port. These values are used in the 
   <b>status</b> member of the 
   <a href="https://msdn.microsoft.com/297ccb5c-3fa2-4bb0-bdd2-60d4685dc55c">VDS_HBAPORT_PROP</a> structure. These states correspond to 
   the HBA_PORTSTATE values in the HBA API.


## -enum-fields




### -field VDS_HPS_UNKNOWN

The HBA port status is unknown.
     

HBA_PORTSTATE_UNKNOWN


### -field VDS_HPS_ONLINE

The HBA port is operational.
     

HBA_PORTSTATE_ONLINE


### -field VDS_HPS_OFFLINE

The HBA port has been set offline by a user.
     

HBA_PORTSTATE_OFFLINE


### -field VDS_HPS_BYPASSED

The HBA port is bypassed.
     

HBA_PORTSTATE_BYPASSED


### -field VDS_HPS_DIAGNOSTICS

The HBA port is in diagnostics mode.
     

HBA_PORTSTATE_DIAGNOSTICS


### -field VDS_HPS_LINKDOWN

The HBA port link is down.
     

HBA_PORTSTATE_LINKDOWN


### -field VDS_HPS_ERROR

The HBA port has an error.
     

HBA_PORTSTATE_ERROR


### -field VDS_HPS_LOOPBACK

The HBA port is loopback.
     

HBA_PORTSTATE_LOOPBACK


## -remarks



<div class="alert"><b>Note</b>  Additional constants might be added to the <b>VDS_HBAPORT_STATUS</b> enumeration in future Windows versions. For this reason, your application must be designed to gracefully handle an unrecognized <b>VDS_HBAPORT_STATUS</b> enumeration constant.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/30ee6e39-c1e5-4173-a3dd-5644632140d1">VDS Enumerations</a>



<a href="https://msdn.microsoft.com/297ccb5c-3fa2-4bb0-bdd2-60d4685dc55c">VDS_HBAPORT_PROP</a>
 

 

