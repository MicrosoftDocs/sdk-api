---
UID: NS:vdshwprv._VDS_PORT_PROP
title: VDS_PORT_PROP (vdshwprv.h)
description: The VDS_PORT_PROP structure (vdshwprv.h) defines the properties of a port on a controller object.
helpviewer_keywords: ["*PVDS_PORT_PROP","VDS_PORT_PROP","VDS_PORT_PROP structure [VDS]","base.vds_port_prop","vds/_VDS_PORT_PROP","vdshwprv/_VDS_PORT_PROP"]
old-location: base\vds_port_prop.htm
tech.root: base
ms.assetid: 40f81f31-3776-4685-8b79-c047c669b2bb
ms.date: 08/08/2022
ms.keywords: '*PVDS_PORT_PROP, VDS_PORT_PROP, VDS_PORT_PROP structure [VDS], base.vds_port_prop, vds/_VDS_PORT_PROP, vdshwprv/_VDS_PORT_PROP'
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
req.typenames: VDS_PORT_PROP, *PVDS_PORT_PROP
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _VDS_PORT_PROP
 - vdshwprv/_VDS_PORT_PROP
 - PVDS_PORT_PROP
 - vdshwprv/PVDS_PORT_PROP
 - VDS_PORT_PROP
 - vdshwprv/VDS_PORT_PROP
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
 - VDS_PORT_PROP
---

# VDS_PORT_PROP structure


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Defines the properties 
   of a port on a controller object.

## -struct-fields

### -field id

The <b>VDS_OBJECT_ID</b> assigned to the port.

### -field pwszFriendlyName

The name of the port; a zero-terminated, human-readable string.

### -field pwszIdentification

The port identifier or address, typically a world wide name (WWN); a zero-terminated, human-readable 
      string.

For Fibre Channel networks, this member should be the WWN for the port, formatted as a hexadecimal string (16 characters long), most significant byte first. For example, a WWN address of 01:23:45:67:89:AB:CD:EF should be represented as "0123456789ABCDEF".

### -field status

The status of the port enumerated by 
      <a href="/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_port_status">VDS_PORT_STATUS</a>.

## -remarks

The 
    <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdscontroller-getportproperties">IVdsController::GetPortProperties</a> 
    method returns this structure to report the property details of a port on a controller object.

## -see-also

<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdscontroller-getportproperties">IVdsController::GetPortProperties</a>



<a href="/windows/desktop/VDS/vds-structures">VDS Structures</a>



<a href="/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_port_status">VDS_PORT_STATUS</a>
