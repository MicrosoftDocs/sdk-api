---
UID: NE:vdslun._VDS_INTERCONNECT_ADDRESS_TYPE
title: "_VDS_INTERCONNECT_ADDRESS_TYPE"
author: windows-sdk-content
description: Defines the set of the valid address types of a physical interconnect.
old-location: base\vds_interconnect_address_type.htm
old-project: VDS
ms.assetid: 20d75585-a80c-49bc-9f9c-5aae8e5f2c21
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: VDS_IA_FCFS, VDS_IA_FCPH, VDS_IA_FCPH3, VDS_IA_MAC, VDS_IA_SCSI, VDS_IA_UNKNOWN, VDS_INTERCONNECT_ADDRESS_TYPE, VDS_INTERCONNECT_ADDRESS_TYPE enumeration [VDS], _VDS_INTERCONNECT_ADDRESS_TYPE, base.vds_interconnect_address_type, vdslun/VDS_IA_FCFS, vdslun/VDS_IA_FCPH, vdslun/VDS_IA_FCPH3, vdslun/VDS_IA_MAC, vdslun/VDS_IA_SCSI, vdslun/VDS_IA_UNKNOWN, vdslun/VDS_INTERCONNECT_ADDRESS_TYPE
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: vdslun.h
req.include-header: Vds.h, VdsHwPrv.h for hardware providers
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
tech.root: 
req.typenames: VDS_INTERCONNECT_ADDRESS_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - VdsLun.h
api_name:
 - VDS_INTERCONNECT_ADDRESS_TYPE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# _VDS_INTERCONNECT_ADDRESS_TYPE enumeration


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Defines the set of the valid address types of a physical interconnect.


## -enum-fields




### -field VDS_IA_UNKNOWN

This value is reserved.


### -field VDS_IA_FCFS

The address type is FCFS.


### -field VDS_IA_FCPH

The address type is FCPH.


### -field VDS_IA_FCPH3

The address type is FCPH3.


### -field VDS_IA_MAC

The address type is MAC.


### -field VDS_IA_SCSI

The address type is SCSI.


## -remarks




    The <a href="https://msdn.microsoft.com/fc9f532b-a37f-4338-95db-6ec988131211">VDS_INTERCONNECT</a> structure includes a <b>VDS_INTERCONNECT_ADDRESS_TYPE</b> value as a member to indicate an interconnect address type.

<div class="alert"><b>Note</b>  Additional constants might be added to the <b>VDS_INTERCONNECT_ADDRESS_TYPE</b> enumeration in future Windows versions. For this reason, your application must be designed to gracefully handle an unrecognized <b>VDS_INTERCONNECT_ADDRESS_TYPE</b> enumeration constant.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/30ee6e39-c1e5-4173-a3dd-5644632140d1">VDS Enumerations</a>



<a href="https://msdn.microsoft.com/fc9f532b-a37f-4338-95db-6ec988131211">VDS_INTERCONNECT</a>
 

 

