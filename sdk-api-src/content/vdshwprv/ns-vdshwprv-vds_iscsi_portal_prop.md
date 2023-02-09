---
UID: NS:vdshwprv._VDS_ISCSI_PORTAL_PROP
title: VDS_ISCSI_PORTAL_PROP (vdshwprv.h)
description: The VDS_ISCSI_PORTAL_PROP structure (vdshwprv.h) defines the properties of an iSCSI portal.
helpviewer_keywords: ["*PVDS_ISCSI_PORTAL_PROP","VDS_ISCSI_PORTAL_PROP","VDS_ISCSI_PORTAL_PROP structure [VDS]","base.vds_iscsi_portal_prop","vds/VDS_ISCSI_PORTAL_PROP","vdshwprv/VDS_ISCSI_PORTAL_PROP"]
old-location: base\vds_iscsi_portal_prop.htm
tech.root: base
ms.assetid: da2d19ca-88a8-4a6a-bbe7-98a9d8af5b1b
ms.date: 08/08/2022
ms.keywords: '*PVDS_ISCSI_PORTAL_PROP, VDS_ISCSI_PORTAL_PROP, VDS_ISCSI_PORTAL_PROP structure [VDS], base.vds_iscsi_portal_prop, vds/VDS_ISCSI_PORTAL_PROP, vdshwprv/VDS_ISCSI_PORTAL_PROP'
req.header: vdshwprv.h
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
req.typenames: VDS_ISCSI_PORTAL_PROP, *PVDS_ISCSI_PORTAL_PROP
req.redist: VDS 1.1
ms.custom: 19H1
f1_keywords:
 - _VDS_ISCSI_PORTAL_PROP
 - vdshwprv/_VDS_ISCSI_PORTAL_PROP
 - PVDS_ISCSI_PORTAL_PROP
 - vdshwprv/PVDS_ISCSI_PORTAL_PROP
 - VDS_ISCSI_PORTAL_PROP
 - vdshwprv/VDS_ISCSI_PORTAL_PROP
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
 - VDS_ISCSI_PORTAL_PROP
---

# VDS_ISCSI_PORTAL_PROP structure


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Defines the properties of an iSCSI portal.

## -struct-fields

### -field id

The <b>VDS_OBJECT_ID</b> of the portal.

### -field address

The IP address and port of the portal.

### -field status

The status of the portal, enumerated by 
     <a href="/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_iscsi_portal_status">VDS_ISCSI_PORTAL_STATUS</a>.

## -see-also

<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsiscsiportal-getproperties">IVdsIscsiPortal::GetProperties</a>



<a href="/windows/desktop/VDS/vds-structures">VDS Structures</a>



<a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_ipaddress">VDS_IPADDRESS</a>



<a href="/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_iscsi_portal_status">VDS_ISCSI_PORTAL_STATUS</a>
