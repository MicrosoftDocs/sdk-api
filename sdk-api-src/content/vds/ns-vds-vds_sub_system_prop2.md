---
UID: NS:vds._VDS_SUB_SYSTEM_PROP2
title: VDS_SUB_SYSTEM_PROP2 (vds.h)
description: The VDS_SUB_SYSTEM_PROP2 structure (vds.h) defines the properties of a subsystem object. 
helpviewer_keywords: ["*PVDS_SUB_SYSTEM_PROP2","PVDS_SUB_SYSTEM_PROP2","PVDS_SUB_SYSTEM_PROP2 structure pointer","VDS_H_DEGRADED","VDS_H_FAILED","VDS_H_HEALTHY","VDS_H_UNKNOWN","VDS_SUB_SYSTEM_PROP2","VDS_SUB_SYSTEM_PROP2 structure","base.vds_sub_system_prop2","vds/PVDS_SUB_SYSTEM_PROP2","vds/VDS_SUB_SYSTEM_PROP2","vdshwprv/PVDS_SUB_SYSTEM_PROP2","vdshwprv/VDS_SUB_SYSTEM_PROP2"]
old-location: base\vds_sub_system_prop2.htm
tech.root: base
ms.assetid: 8eb743b5-26e6-42e5-b94b-0849b1280cdb
ms.date: 08/05/2022
ms.keywords: '*PVDS_SUB_SYSTEM_PROP2, PVDS_SUB_SYSTEM_PROP2, PVDS_SUB_SYSTEM_PROP2 structure pointer, VDS_H_DEGRADED, VDS_H_FAILED, VDS_H_HEALTHY, VDS_H_UNKNOWN, VDS_SUB_SYSTEM_PROP2, VDS_SUB_SYSTEM_PROP2 structure, base.vds_sub_system_prop2, vds/PVDS_SUB_SYSTEM_PROP2, vds/VDS_SUB_SYSTEM_PROP2, vdshwprv/PVDS_SUB_SYSTEM_PROP2, vdshwprv/VDS_SUB_SYSTEM_PROP2'
req.header: vds.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: VDS_SUB_SYSTEM_PROP2, *PVDS_SUB_SYSTEM_PROP2
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _VDS_SUB_SYSTEM_PROP2
 - vds/_VDS_SUB_SYSTEM_PROP2
 - PVDS_SUB_SYSTEM_PROP2
 - vds/PVDS_SUB_SYSTEM_PROP2
 - VDS_SUB_SYSTEM_PROP2
 - vds/VDS_SUB_SYSTEM_PROP2
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
 - VDS_SUB_SYSTEM_PROP2
---

# VDS_SUB_SYSTEM_PROP2 structure


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Defines the 
   properties of a <a href="/windows/desktop/VDS/subsystem-object">subsystem object</a>. This structure is identical to the <a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_sub_system_prop">VDS_SUB_SYSTEM_PROP</a> structure, except that it includes the supported RAID types and number of enclosures as members.

## -struct-fields

### -field id

The GUID of the subsystem object.

### -field pwszFriendlyName

A pointer to a <b>NULL</b>-terminated wide-character string containing the name of the subsystem, typically a brand name and a model name.

### -field pwszIdentification

A pointer to a <b>NULL</b>-terminated wide-character string containing a combination of the  disk array's serial number and the subsystem identifier.

### -field ulFlags

A bitmask of one or more   
      <a href="/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_sub_system_flag">VDS_SUB_SYSTEM_FLAG</a> enumeration values.

### -field ulStripeSizeFlags

The set of stripe sizes supported by a provider for striped volumes and/or LUNs. A stripe size must be a 
      power of 2. Each bit in the 32-bit integer represents a size, in bytes. For example, if the <i>n</i>th 
      bit is set, then VDS supports stripe size of 2^<i>n</i>. Thus, bits 0 through 31 can specify 
      2^0 through 2^31.

### -field ulSupportedRaidTypeFlags

A bitmask of  <a href="/windows/win32/api/vdshwprv/ne-vdshwprv-vds_sub_system_supported_raid_type_flag">VDS_SUB_SYSTEM_SUPPORTED_RAID_TYPE_FLAG</a> enumeration values specifying the RAID levels that the subsystem supports.  The default value for this member is zero. A value of zero means that no RAID levels are supported.

### -field status

A <a href="/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_sub_system_status">VDS_SUB_SYSTEM_STATUS</a> enumeration value that specifies the status of the subsystem object.

### -field health

A <a href="/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_health">VDS_HEALTH</a> enumeration value that specifies the health state of the subsystem. The following are the valid values for this member.



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

### -field ulNumberOfEnclosures

The number of enclosures in the subsystem. The default value for this member is zero. A value of zero indicates that this property is not available for this subsystem.

## -remarks

The <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdssubsystem2-getproperties2">IVdsSubSystem2::GetProperties2</a> 
    method returns this structure to report the properties of a <a href="/windows/desktop/VDS/subsystem-object">subsystem object</a>.

## -see-also

<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdssubsystem-getproperties">IVdsSubSystem::GetProperties</a>



<a href="/windows/desktop/VDS/vds-structures">VDS Structures</a>



<a href="/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_health">VDS_HEALTH</a>



<a href="/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_sub_system_status">VDS_SUB_SYSTEM_STATUS</a>
