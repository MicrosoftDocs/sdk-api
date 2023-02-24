---
UID: NS:vds._VDS_ISCSI_INITIATOR_PORTAL_PROP
title: VDS_ISCSI_INITIATOR_PORTAL_PROP (vds.h)
description: The VDS_ISCSI_INITIATOR_PORTAL_PROP structure (vds.h) defines the properties of an iSCSI initiator portal.
helpviewer_keywords: ["VDS_ISCSI_INITIATOR_PORTAL_PROP","VDS_ISCSI_INITIATOR_PORTAL_PROP structure [VDS]","_VDS_ISCSI_INITIATOR_PORTAL_PROP","base.vds_iscsi_initiator_portal_prop","vds/VDS_ISCSI_INITIATOR_PORTAL_PROP","vdshwprv/VDS_ISCSI_INITIATOR_PORTAL_PROP"]
old-location: base\vds_iscsi_initiator_portal_prop.htm
tech.root: base
ms.assetid: 58fffdb4-71c4-4f84-ad0e-7efe5bdb78a7
ms.date: 08/05/2022
ms.keywords: VDS_ISCSI_INITIATOR_PORTAL_PROP, VDS_ISCSI_INITIATOR_PORTAL_PROP structure [VDS], _VDS_ISCSI_INITIATOR_PORTAL_PROP, base.vds_iscsi_initiator_portal_prop, vds/VDS_ISCSI_INITIATOR_PORTAL_PROP, vdshwprv/VDS_ISCSI_INITIATOR_PORTAL_PROP
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
req.typenames: VDS_ISCSI_INITIATOR_PORTAL_PROP
req.redist: VDS 1.1
ms.custom: 19H1
f1_keywords:
 - _VDS_ISCSI_INITIATOR_PORTAL_PROP
 - vds/_VDS_ISCSI_INITIATOR_PORTAL_PROP
 - VDS_ISCSI_INITIATOR_PORTAL_PROP
 - vds/VDS_ISCSI_INITIATOR_PORTAL_PROP
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
 - VDS_ISCSI_INITIATOR_PORTAL_PROP
---

# VDS_ISCSI_INITIATOR_PORTAL_PROP structure


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Defines the properties of an iSCSI initiator portal.

## -struct-fields

### -field id

The <b>VDS_OBJECT_ID</b> assigned to the initiator portal.

### -field address

The IP address and port of the portal.

### -field ulPortIndex

The port index assigned to the portal by the iSCSI initiator service.

## -see-also

<a href="/windows/desktop/api/vds/nf-vds-ivdsiscsiinitiatorportal-getproperties">IVdsIscsiInitiatorPortal::GetProperties</a>



<a href="/windows/desktop/VDS/vds-structures">VDS Structures</a>



<a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_ipaddress">VDS_IPADDRESS</a>
