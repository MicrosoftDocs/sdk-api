---
UID: NE:vdshwprv._VDS_LUN_PLEX_STATUS
title: "_VDS_LUN_PLEX_STATUS"
author: windows-driver-content
description: Defines the set of object status values for a LUN plex.
old-location: base\vds_lun_plex_status.htm
old-project: VDS
ms.assetid: 04eed033-45b3-42bc-a304-25525cddd085
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: VDS_LPS_FAILED, VDS_LPS_NOT_READY, VDS_LPS_OFFLINE, VDS_LPS_ONLINE, VDS_LPS_UNKNOWN, VDS_LUN_PLEX_STATUS, VDS_LUN_PLEX_STATUS enumeration [VDS], _VDS_LUN_PLEX_STATUS, base.vds_lun_plex_status, vds/VDS_LPS_FAILED, vds/VDS_LPS_NOT_READY, vds/VDS_LPS_OFFLINE, vds/VDS_LPS_ONLINE, vds/VDS_LPS_UNKNOWN, vds/VDS_LUN_PLEX_STATUS, vdshwprv/VDS_LPS_FAILED, vdshwprv/VDS_LPS_NOT_READY, vdshwprv/VDS_LPS_OFFLINE, vdshwprv/VDS_LPS_ONLINE, vdshwprv/VDS_LPS_UNKNOWN, vdshwprv/VDS_LUN_PLEX_STATUS
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: vdshwprv.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: VDS_LUN_PLEX_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Vds.h
-	VdsHwPrv.h
api_name:
-	VDS_LUN_PLEX_STATUS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# _VDS_LUN_PLEX_STATUS enumeration


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Defines the set of object status values for a LUN plex.


## -enum-fields




### -field VDS_LPS_UNKNOWN

This value is reserved.


### -field VDS_LPS_ONLINE

The plex is available.


### -field VDS_LPS_NOT_READY

The plex is busy.


### -field VDS_LPS_OFFLINE

The plex is unavailable.


### -field VDS_LPS_FAILED

The plex has failed.


## -remarks



The <a href="https://msdn.microsoft.com/d79ce5a9-af5a-4691-b853-c18d4a4d04c7">VDS_LUN_PLEX_PROP</a>
       structure includes a <b>VDS_LUN_PLEX_STATUS</b> value as a member to indicate the current status of the LUN plex.

<div class="alert"><b>Note</b>  Additional constants might be added to the <b>VDS_LUN_PLEX_STATUS</b> enumeration in future Windows versions. For this reason, your application must be designed to gracefully handle an unrecognized <b>VDS_LUN_PLEX_STATUS</b> enumeration constant.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/30ee6e39-c1e5-4173-a3dd-5644632140d1">VDS Enumerations</a>



<a href="https://msdn.microsoft.com/d79ce5a9-af5a-4691-b853-c18d4a4d04c7">
        VDS_LUN_PLEX_PROP</a>
 

 

