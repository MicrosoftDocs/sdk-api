---
UID: NS:vdshwprv._VDS_LUN_PROP
title: VDS_LUN_PROP (vdshwprv.h)
description: The VDS_LUN_PROP structure (vdshwprv.h) defines the properties of a LUN object.
helpviewer_keywords: ["*PVDS_LUN_PROP","PVDS_LUN_PROP","PVDS_LUN_PROP structure pointer [VDS]","VDS_H_FAILED","VDS_H_FAILED_REDUNDANCY","VDS_H_FAILED_REDUNDANCY_FAILING","VDS_H_FAILING","VDS_H_FAILING_REDUNDANCY","VDS_H_HEALTHY","VDS_H_REBUILDING","VDS_H_UNKNOWN","VDS_LUN_PROP","VDS_LUN_PROP structure [VDS]","base.vds_lun_prop","vds/PVDS_LUN_PROP","vds/_VDS_LUN_PROP","vdshwprv/PVDS_LUN_PROP","vdshwprv/_VDS_LUN_PROP"]
old-location: base\vds_lun_prop.htm
tech.root: base
ms.assetid: 4ef0f4d8-7c63-4d8e-bf46-e6958661bd6a
ms.date: 08/08/2022
ms.keywords: '*PVDS_LUN_PROP, PVDS_LUN_PROP, PVDS_LUN_PROP structure pointer [VDS], VDS_H_FAILED, VDS_H_FAILED_REDUNDANCY, VDS_H_FAILED_REDUNDANCY_FAILING, VDS_H_FAILING, VDS_H_FAILING_REDUNDANCY, VDS_H_HEALTHY, VDS_H_REBUILDING, VDS_H_UNKNOWN, VDS_LUN_PROP, VDS_LUN_PROP structure [VDS], base.vds_lun_prop, vds/PVDS_LUN_PROP, vds/_VDS_LUN_PROP, vdshwprv/PVDS_LUN_PROP, vdshwprv/_VDS_LUN_PROP'
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
req.typenames: VDS_LUN_PROP, *PVDS_LUN_PROP
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _VDS_LUN_PROP
 - vdshwprv/_VDS_LUN_PROP
 - PVDS_LUN_PROP
 - vdshwprv/PVDS_LUN_PROP
 - VDS_LUN_PROP
 - vdshwprv/VDS_LUN_PROP
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
 - VDS_LUN_PROP
---

# VDS_LUN_PROP structure


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Defines the properties of 
   a <a href="/windows/desktop/VDS/lun-object">LUN object</a>.

## -struct-fields

### -field id

The GUID of the LUN object.

### -field ullSize

The size of the LUN, in bytes.

### -field pwszFriendlyName

The name of the LUN; a zero-terminated, human-readable string.

### -field pwszIdentification

The unique LUN identifier; a zero-terminated, human-readable string.

### -field pwszUnmaskingList

A list specifying the computers on the network to be granted access the LUN; a semicolon-delimited, 
      NULL-terminated, human-readable string. 

If the value is "*", all computers on the network are to be granted 
      access to the LUN. If the value is "", no computers are to be granted access to the LUN.

<div class="alert"><b>Note</b>  In practice, if the value is "*", most hardware providers only grant the ports and initiators on the local computer access to the LUN.</div>
<div> </div>
If "*" or "" is specified, no other value can be specified.

For Fibre Channel networks and serial attached SCSI (SAS) networks, each entry is a 64-bit World-Wide Name (WWN) of each port to which the LUN is unmasked, 
       formatted as a hexadecimal string (16 characters long), most significant byte first. For 
       example, a WWN address of 01:23:45:67:89:AB:CD:EF is represented as "0123456789ABCDEF". For more information, see the T10 specifications for <a href="https://t10.org/drafts.htm#FibreChannel">Fibre Channel</a> and <a href="https://t10.org/drafts.htm#SCSI3_SAS">SAS</a>.

For iSCSI networks, each entry is an iSCSI qualified name (IQN) of each initiator to which the LUN is unmasked. A LUN unmasked 
       to a particular initiator is considered to be associated with that initiator.

<div class="alert"><b>Note</b>  The unmasking list can contain the same WWN or IQN more than once. Duplicates are ignored.</div>
<div> </div>

### -field ulFlags

The LUN flags enumerated by <a href="/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_lun_flag">VDS_LUN_FLAG</a>.

### -field type

The LUN type enumerated by <a href="/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_lun_type">VDS_LUN_TYPE</a>.

### -field status

The status of the LUN object enumerated by 
      <a href="/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_lun_status">VDS_LUN_STATUS</a>.

### -field health

A 
      <a href="/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_health">VDS_HEALTH</a> enumeration value that specifies the health state of the LUN. The following are the valid values for this member.



#### VDS_H_UNKNOWN (0)



#### VDS_H_HEALTHY (1)



#### VDS_H_REBUILDING (2)



#### VDS_H_FAILING (4)



#### VDS_H_FAILING_REDUNDANCY (5)



#### VDS_H_FAILED_REDUNDANCY (6)



#### VDS_H_FAILED_REDUNDANCY_FAILING (7)



#### VDS_H_FAILED (8)

### -field TransitionState

The transition state of the LUN enumerated by
      <a href="/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_transition_state">VDS_TRANSITION_STATE</a>.

### -field sRebuildPriority

The rebuild priority of the LUN object. A value between 0 (lowest priority) and 15 (highest priority).


##### - health.VDS_H_FAILED (8)


##### - health.VDS_H_FAILED_REDUNDANCY (6)


##### - health.VDS_H_FAILED_REDUNDANCY_FAILING (7)


##### - health.VDS_H_FAILING (4)


##### - health.VDS_H_FAILING_REDUNDANCY (5)


##### - health.VDS_H_HEALTHY (1)


##### - health.VDS_H_REBUILDING (2)


##### - health.VDS_H_UNKNOWN (0)

## -remarks

The <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdslun-getproperties">IVdsLun::GetProperties</a> method returns 
    this structure to report the properties of a <a href="/windows/desktop/VDS/lun-object">LUN object</a>.

## -see-also

<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdslun-getproperties">IVdsLun::GetProperties</a>



<a href="/windows/desktop/VDS/vds-structures">VDS Structures</a>



<a href="/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_health">VDS_HEALTH</a>



<a href="/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_lun_status">VDS_LUN_STATUS</a>



<a href="/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_lun_type">VDS_LUN_TYPE</a>



<a href="/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_transition_state">VDS_TRANSITION_STATE</a>
