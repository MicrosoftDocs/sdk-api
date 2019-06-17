---
UID: NE:vdslun._VDS_INTERCONNECT_ADDRESS_TYPE
title: VDS_INTERCONNECT_ADDRESS_TYPE (vdslun.h)
author: windows-sdk-content
description: Defines the set of the valid address types of a physical interconnect.
old-location: base\vds_interconnect_address_type.htm
tech.root: VDS
ms.assetid: 20d75585-a80c-49bc-9f9c-5aae8e5f2c21
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: VDS_IA_FCFS, VDS_IA_FCPH, VDS_IA_FCPH3, VDS_IA_MAC, VDS_IA_SCSI, VDS_IA_UNKNOWN, VDS_INTERCONNECT_ADDRESS_TYPE, VDS_INTERCONNECT_ADDRESS_TYPE enumeration [VDS], base.vds_interconnect_address_type, vdslun/VDS_IA_FCFS, vdslun/VDS_IA_FCPH, vdslun/VDS_IA_FCPH3, vdslun/VDS_IA_MAC, vdslun/VDS_IA_SCSI, vdslun/VDS_IA_UNKNOWN, vdslun/VDS_INTERCONNECT_ADDRESS_TYPE
ms.topic: enum
f1_keywords: ["vdslun/VDS_INTERCONNECT_ADDRESS_TYPE"]
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
req.lib: 
req.dll: 
req.irql: 
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
req.typenames: VDS_INTERCONNECT_ADDRESS_TYPE
req.redist: 
ms.custom: 19H1
---

# VDS_INTERCONNECT_ADDRESS_TYPE enumeration


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://docs.microsoft.com/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

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



The <a href="https://docs.microsoft.com/windows/desktop/api/vdslun/ns-vdslun-_vds_interconnect">VDS_INTERCONNECT</a> structure includes a <b>VDS_INTERCONNECT_ADDRESS_TYPE</b> value as a member to indicate an interconnect address type.

<div class="alert"><b>Note</b>  Additional constants might be added to the <b>VDS_INTERCONNECT_ADDRESS_TYPE</b> enumeration in future Windows versions. For this reason, your application must be designed to gracefully handle an unrecognized <b>VDS_INTERCONNECT_ADDRESS_TYPE</b> enumeration constant.</div>
<div> </div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/VDS/vds-enumerations">VDS Enumerations</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vdslun/ns-vdslun-_vds_interconnect">VDS_INTERCONNECT</a>
 

 

