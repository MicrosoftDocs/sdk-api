---
UID: NS:vdshwprv._VDS_CONTROLLER_PROP
title: VDS_CONTROLLER_PROP (vdshwprv.h)
description: The VDS_CONTROLLER_PROP structure (vdshwprv.h) defines the properties of a controller object. 
helpviewer_keywords: ["*PVDS_CONTROLLER_PROP","VDS_CONTROLLER_PROP","VDS_CONTROLLER_PROP structure [VDS]","VDS_H_DEGRADED","VDS_H_FAILED","VDS_H_HEALTHY","VDS_H_REPLACED","VDS_H_UNKNOWN","base.vds_controller_prop","vds/_VDS_CONTROLLER_PROP","vdshwprv/_VDS_CONTROLLER_PROP"]
old-location: base\vds_controller_prop.htm
tech.root: base
ms.assetid: b9da3920-9bae-4198-ba0d-a0755aee15e4
ms.date: 08/08/2022
ms.keywords: '*PVDS_CONTROLLER_PROP, VDS_CONTROLLER_PROP, VDS_CONTROLLER_PROP structure [VDS], VDS_H_DEGRADED, VDS_H_FAILED, VDS_H_HEALTHY, VDS_H_REPLACED, VDS_H_UNKNOWN, base.vds_controller_prop, vds/_VDS_CONTROLLER_PROP, vdshwprv/_VDS_CONTROLLER_PROP'
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
req.typenames: VDS_CONTROLLER_PROP, *PVDS_CONTROLLER_PROP
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _VDS_CONTROLLER_PROP
 - vdshwprv/_VDS_CONTROLLER_PROP
 - PVDS_CONTROLLER_PROP
 - vdshwprv/PVDS_CONTROLLER_PROP
 - VDS_CONTROLLER_PROP
 - vdshwprv/VDS_CONTROLLER_PROP
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
 - VDS_CONTROLLER_PROP
---

# VDS_CONTROLLER_PROP structure


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Defines the 
   properties of a <a href="/windows/desktop/VDS/controller-object">controller object</a>.

## -struct-fields

### -field id

The GUID of the controller object.

### -field pwszFriendlyName

The name of the controller; a zero-terminated, human-readable string.

### -field pwszIdentification

The subsystem identifier, typically a serial number; a zero-terminated, human-readable string.

### -field status

A 
      <a href="/windows/desktop/api/vds/ne-vds-vds_controller_status">VDS_CONTROLLER_STATUS</a> enumeration value that specifies the status of the controller.

### -field health

A 
      <a href="/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_health">VDS_HEALTH</a> enumeration value that specifies the health state of the controller. The following are the valid values for this member.

<b>Windows Server 2008, Windows Vista and Windows Server 2003:  </b><b>VDS_H_REPLACED</b> and <b>VDS_H_DEGRADED</b> are not supported.



#### VDS_H_UNKNOWN (0)



#### VDS_H_HEALTHY (1)



#### VDS_H_FAILED (8)



#### VDS_H_REPLACED (9)



#### VDS_H_DEGRADED (11)

### -field sNumberOfPorts

The number of ports that the controller contains. Ports are numbered from zero. Hardware providers should set this member to zero for PCI RAID cards.


##### - health.VDS_H_DEGRADED (11)


##### - health.VDS_H_FAILED (8)


##### - health.VDS_H_HEALTHY (1)


##### - health.VDS_H_REPLACED (9)


##### - health.VDS_H_UNKNOWN (0)

## -remarks

The <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdscontroller-getproperties">IVdsController::GetProperties</a> 
    method returns this structure to report the properties of a <a href="/windows/desktop/VDS/controller-object">controller object</a>.

## -see-also

<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdscontroller-getproperties">IVdsController::GetProperties</a>



<a href="/windows/desktop/VDS/vds-structures">VDS Structures</a>



<a href="/windows/desktop/api/vds/ne-vds-vds_controller_status">VDS_CONTROLLER_STATUS</a>



<a href="/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_health">VDS_HEALTH</a>
