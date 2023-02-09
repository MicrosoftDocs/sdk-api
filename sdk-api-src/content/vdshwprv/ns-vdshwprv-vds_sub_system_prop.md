---
UID: NS:vdshwprv._VDS_SUB_SYSTEM_PROP
title: VDS_SUB_SYSTEM_PROP (vdshwprv.h)
description: The VDS_SUB_SYSTEM_PROP structure (vdshwprv.h) defines the properties of a subsystem object.
helpviewer_keywords: ["*PVDS_SUB_SYSTEM_PROP","VDS_H_DEGRADED","VDS_H_FAILED","VDS_H_HEALTHY","VDS_H_UNKNOWN","VDS_SUB_SYSTEM_PROP","VDS_SUB_SYSTEM_PROP structure [VDS]","base.vds_sub_system_prop","vds/_VDS_SUB_SYSTEM_PROP","vdshwprv/_VDS_SUB_SYSTEM_PROP"]
old-location: base\vds_sub_system_prop.htm
tech.root: base
ms.assetid: 8fecb874-5c59-4f55-b528-040ff9209612
ms.date: 08/09/2022
ms.keywords: '*PVDS_SUB_SYSTEM_PROP, VDS_H_DEGRADED, VDS_H_FAILED, VDS_H_HEALTHY, VDS_H_UNKNOWN, VDS_SUB_SYSTEM_PROP, VDS_SUB_SYSTEM_PROP structure [VDS], base.vds_sub_system_prop, vds/_VDS_SUB_SYSTEM_PROP, vdshwprv/_VDS_SUB_SYSTEM_PROP'
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: VDS_SUB_SYSTEM_PROP, *PVDS_SUB_SYSTEM_PROP
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _VDS_SUB_SYSTEM_PROP
 - vdshwprv/_VDS_SUB_SYSTEM_PROP
 - PVDS_SUB_SYSTEM_PROP
 - vdshwprv/PVDS_SUB_SYSTEM_PROP
 - VDS_SUB_SYSTEM_PROP
 - vdshwprv/VDS_SUB_SYSTEM_PROP
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Vds.h
 - VdsHwPrv.h
api_name:
 - VDS_SUB_SYSTEM_PROP
---

# VDS_SUB_SYSTEM_PROP structure


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Defines the 
   properties of a <a href="/windows/desktop/VDS/subsystem-object">subsystem object</a>.

## -struct-fields

### -field id

The GUID of the subsystem object.

### -field pwszFriendlyName

The name of the subsystem, typically a brand name and a model name; a zero-terminated, human-readable 
      string.

### -field pwszIdentification

The subsystem identifier; a zero-terminated, human-readable string.

### -field ulFlags

A bitmask of one or more   
      <a href="/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_sub_system_flag">VDS_SUB_SYSTEM_FLAG</a> enumeration values.

### -field ulStripeSizeFlags

The set of stripe sizes supported by a provider for striped volumes and/or LUNs. A stripe size must be a 
      power of 2. Each bit in the 32-bit integer represents a size, in bytes. For example, if the <i>n</i>th 
      bit is set, then VDS supports stripe size of 2^<i>n</i>. Thus, bits 0 through 31 can specify 
      2^0 through 2^31.

### -field status

A <a href="/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_sub_system_status">VDS_SUB_SYSTEM_STATUS</a> enumeration value that specifies the status of the subsystem object.

### -field health

A 
      <a href="/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_health">VDS_HEALTH</a> enumeration value that specifies the health state of the subsystem. The following are the valid values for this member.



#### VDS_H_UNKNOWN (0)



#### VDS_H_HEALTHY (1)



#### VDS_H_FAILED (8)



#### VDS_H_DEGRADED (11)

### -field sNumberOfInternalBuses

The number of buses (or "channels") that the subsystem contains.

### -field sMaxNumberOfSlotsEachBus

The maximum number of slots that each of the buses can include. Each slot can accommodate one drive. The subsystem 
      model assumes that each bus has the same maximum number of slots.

### -field sMaxNumberOfControllers

The maximum number of controllers that the subsystem can contain.

### -field sRebuildPriority

The rebuild priority of the LUNs that belong to the subsystem. This value can range from 0 (lowest priority) through 15 (highest priority).


##### - health.VDS_H_DEGRADED (11)


##### - health.VDS_H_FAILED (8)


##### - health.VDS_H_HEALTHY (1)


##### - health.VDS_H_UNKNOWN (0)

## -remarks

The <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdssubsystem-getproperties">IVdsSubSystem::GetProperties</a> 
    method returns this structure to report the properties of a <a href="/windows/desktop/VDS/subsystem-object">subsystem object</a>.

## -see-also

<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdssubsystem-getproperties">IVdsSubSystem::GetProperties</a>



<a href="/windows/desktop/VDS/vds-structures">VDS Structures</a>



<a href="/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_health">VDS_HEALTH</a>



<a href="/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_sub_system_status">VDS_SUB_SYSTEM_STATUS</a>
