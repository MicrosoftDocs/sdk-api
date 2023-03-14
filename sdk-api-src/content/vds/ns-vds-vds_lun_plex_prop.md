---
UID: NS:vds._VDS_LUN_PLEX_PROP
title: VDS_LUN_PLEX_PROP (vds.h)
description: The VDS_LUN_PLEX_PROP structure (vds.h) defines the properties of a LUN plex object. 
helpviewer_keywords: ["*PVDS_LUN_PLEX_PROP","VDS_H_FAILED","VDS_H_FAILED_REDUNDANCY","VDS_H_FAILED_REDUNDANCY_FAILING","VDS_H_FAILING","VDS_H_FAILING_REDUNDANCY","VDS_H_HEALTHY","VDS_H_REBUILDING","VDS_H_UNKNOWN","VDS_LUN_PLEX_PROP","VDS_LUN_PLEX_PROP structure [VDS]","base.vds_lun_plex_prop","vds/_VDS_LUN_PLEX_PROP","vdshwprv/_VDS_LUN_PLEX_PROP"]
old-location: base\vds_lun_plex_prop.htm
tech.root: base
ms.assetid: d79ce5a9-af5a-4691-b853-c18d4a4d04c7
ms.date: 08/05/2022
ms.keywords: '*PVDS_LUN_PLEX_PROP, VDS_H_FAILED, VDS_H_FAILED_REDUNDANCY, VDS_H_FAILED_REDUNDANCY_FAILING, VDS_H_FAILING, VDS_H_FAILING_REDUNDANCY, VDS_H_HEALTHY, VDS_H_REBUILDING, VDS_H_UNKNOWN, VDS_LUN_PLEX_PROP, VDS_LUN_PLEX_PROP structure [VDS], base.vds_lun_plex_prop, vds/_VDS_LUN_PLEX_PROP, vdshwprv/_VDS_LUN_PLEX_PROP'
req.header: vds.h
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
req.typenames: VDS_LUN_PLEX_PROP, *PVDS_LUN_PLEX_PROP
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _VDS_LUN_PLEX_PROP
 - vds/_VDS_LUN_PLEX_PROP
 - PVDS_LUN_PLEX_PROP
 - vds/PVDS_LUN_PLEX_PROP
 - VDS_LUN_PLEX_PROP
 - vds/VDS_LUN_PLEX_PROP
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
 - VDS_LUN_PLEX_PROP
---

# VDS_LUN_PLEX_PROP structure


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Defines the properties of a <a href="/windows/desktop/VDS/lun-plex-object">LUN plex object</a>.

## -struct-fields

### -field id

The GUID of the plex object.

### -field ullSize

The size of the plex, in bytes. The size of the plex can be equal to or greater than that of the LUN to which the plex belongs. The plex cannot be smaller than the LUN.

### -field type

A <a href="/windows/desktop/api/vds/ne-vds-vds_lun_plex_type">VDS_LUN_PLEX_TYPE</a> enumeration value that specifies the type of the plex. The type of the plex is not required to match the type of the LUN to which it belongs.

### -field status

A <a href="/windows/desktop/api/vds/ne-vds-vds_lun_plex_status">VDS_LUN_PLEX_STATUS</a> enumeration value that specifies the status of the plex. The status of the plex is not required to match the status of the LUN to which it belongs.

### -field health

<a href="/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_health">VDS_HEALTH</a>


#### VDS_H_UNKNOWN (0)



#### VDS_H_HEALTHY (1)



#### VDS_H_REBUILDING (2)



#### VDS_H_FAILING (4)



#### VDS_H_FAILING_REDUNDANCY (5)



#### VDS_H_FAILED_REDUNDANCY (6)



#### VDS_H_FAILED_REDUNDANCY_FAILING (7)



#### VDS_H_FAILED (8)

### -field TransitionState

A <a href="/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_transition_state">VDS_TRANSITION_STATE</a> enumeration value that specifies the transition state of the plex.  The transition state of the plex is not required to match that of the LUN to which the plex belongs.

### -field ulFlags

A bitmask of <a href="/windows/desktop/api/vds/ne-vds-vds_lun_plex_flag">VDS_LUN_PLEX_FLAG</a> enumeration values that describe the plex.

### -field ulStripeSize

The stripe interleave size, in bytes. This member is valid only for plexes of type <b>VDS_LPT_STRIPE</b> (striped) and <b>VDS_LPT_PARITY</b> (striped with parity). For other plex types, this member should be zero.

### -field sRebuildPriority

The rebuild priority of the plex. This value must be greater than or equal to 0 (lowest priority) and less than or equal to 15 (highest priority).

## -remarks

The <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdslunplex-getproperties">IVdsLunPlex::GetProperties</a> method returns this structure to report the properties of a <a href="/windows/desktop/VDS/lun-plex-object">LUN plex object</a>.

## -see-also

<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdslunplex-getproperties">IVdsLunPlex::GetProperties</a>



<a href="/windows/desktop/VDS/vds-structures">VDS Structures</a>



<a href="/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_health">VDS_HEALTH</a>



<a href="/windows/desktop/api/vds/ne-vds-vds_lun_plex_flag">VDS_LUN_PLEX_FLAG</a>



<a href="/windows/desktop/api/vds/ne-vds-vds_lun_plex_status">VDS_LUN_PLEX_STATUS</a>



<a href="/windows/desktop/api/vds/ne-vds-vds_lun_plex_type">VDS_LUN_PLEX_TYPE</a>



<a href="/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_transition_state">VDS_TRANSITION_STATE</a>
