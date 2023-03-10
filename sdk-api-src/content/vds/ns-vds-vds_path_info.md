---
UID: NS:vds._VDS_PATH_INFO
title: VDS_PATH_INFO (vds.h)
description: The VDS_PATH_INFO structure (vds.h) defines the information for a LUN path. 
helpviewer_keywords: ["VDS_PATH_INFO","VDS_PATH_INFO structure","base.vds_path_info","vds/VDS_PATH_INFO","vdshwprv/VDS_PATH_INFO"]
old-location: base\vds_path_info.htm
tech.root: base
ms.assetid: 14444252-11ca-4614-81d1-9a15e76d0186
ms.date: 08/05/2022
ms.keywords: VDS_PATH_INFO, VDS_PATH_INFO structure, base.vds_path_info, vds/VDS_PATH_INFO, vdshwprv/VDS_PATH_INFO
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: VDS_PATH_INFO
req.redist: VDS 1.1
ms.custom: 19H1
f1_keywords:
 - _VDS_PATH_INFO
 - vds/_VDS_PATH_INFO
 - VDS_PATH_INFO
 - vds/VDS_PATH_INFO
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
 - VDS_PATH_INFO
---

# VDS_PATH_INFO structure


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Defines the 
   information for a LUN path. This structure is returned in the <i>ppPaths</i> parameter of the <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdslunmpio-getpathinfo">IVdsLunMpio::GetPathInfo</a>  method.

## -struct-fields

### -field pathId

The unique ID of the path used by MPIO.

### -field type

The type of interconnect that the hardware provider supports for this LUN path. <a href="/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_hwprovider_type">VDS_HWT_HYBRID</a> is not a valid value for this member, even if the provider is a hybrid provider.

### -field status

The status of the path, enumerated by 
      <a href="/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_path_status">VDS_PATH_STATUS</a>.

### -field controllerPortId

The <b>VDS_OBJECT_ID</b> of the controller port object on the other end of the 
       path.

### -field targetPortalId

The <b>VDS_OBJECT_ID</b> of the target portal object on the other end of the 
       path.

### -field hbaPortId

The <b>VDS_OBJECT_ID</b> of the HBA port.

### -field initiatorAdapterId

The <b>VDS_OBJECT_ID</b> of the initiator adapter.

### -field pHbaPortProp

A pointer to a <a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_hbaport_prop">VDS_HBAPORT_PROP</a> structure 
       containing properties of the HBA port on one end of the path.

### -field pInitiatorPortalIpAddr

A pointer to a <a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_ipaddress">VDS_IPADDRESS</a> structure containing 
       the IP address and port information for the initiator portal.

## -see-also

<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdslunmpio-getpathinfo">IVdsLunMpio::GetPathInfo</a>



<a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_hbaport_prop">VDS_HBAPORT_PROP</a>



<a href="/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_hwprovider_type">VDS_HWPROVIDER_TYPE</a>



<a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_ipaddress">VDS_IPADDRESS</a>



<a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_path_id">VDS_PATH_ID</a>



<a href="/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_path_status">VDS_PATH_STATUS</a>
