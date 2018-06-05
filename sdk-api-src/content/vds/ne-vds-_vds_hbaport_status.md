---
UID: NE:vds._VDS_HBAPORT_STATUS
title: "_VDS_HBAPORT_STATUS"
author: windows-sdk-content
description: Defines the set of valid statuses for an HBA port.
old-location: base\vds_hbaport_status.htm
old-project: VDS
ms.assetid: 67ef9025-c929-476b-8644-7e085dff91c4
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: VDS_HBAPORT_STATUS, VDS_HBAPORT_STATUS enumeration [VDS], VDS_HPS_BYPASSED, VDS_HPS_DIAGNOSTICS, VDS_HPS_ERROR, VDS_HPS_LINKDOWN, VDS_HPS_LOOPBACK, VDS_HPS_OFFLINE, VDS_HPS_ONLINE, VDS_HPS_UNKNOWN, _VDS_HBAPORT_STATUS, base.vds_hbaport_status, vds/VDS_HBAPORT_STATUS, vds/VDS_HPS_BYPASSED, vds/VDS_HPS_DIAGNOSTICS, vds/VDS_HPS_ERROR, vds/VDS_HPS_LINKDOWN, vds/VDS_HPS_LOOPBACK, vds/VDS_HPS_OFFLINE, vds/VDS_HPS_ONLINE, vds/VDS_HPS_UNKNOWN, vdshwprv/VDS_HBAPORT_STATUS, vdshwprv/VDS_HPS_BYPASSED, vdshwprv/VDS_HPS_DIAGNOSTICS, vdshwprv/VDS_HPS_ERROR, vdshwprv/VDS_HPS_LINKDOWN, vdshwprv/VDS_HPS_LOOPBACK, vdshwprv/VDS_HPS_OFFLINE, vdshwprv/VDS_HPS_ONLINE, vdshwprv/VDS_HPS_UNKNOWN
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: vds.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: VDS_HBAPORT_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Vds.h
-	VdsHwPrv.h
api_name:
-	VDS_HBAPORT_STATUS
product: Windows
targetos: Windows
req.lib: VdmDbg.lib
req.dll: VdmDbg.dll
req.irql: 
req.product: Windows UI
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
 

 

