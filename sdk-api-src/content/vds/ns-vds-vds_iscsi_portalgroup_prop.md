---
UID: NS:vds._VDS_ISCSI_PORTALGROUP_PROP
title: VDS_ISCSI_PORTALGROUP_PROP (vds.h)
description: The VDS_ISCSI_PORTALGROUP_PROP structure (vds.h) defines the properties of an iSCSI portal group. 
helpviewer_keywords: ["*PVDS_ISCSI_PORTALGROUP_PROP","VDS_ISCSI_PORTALGROUP_PROP","VDS_ISCSI_PORTALGROUP_PROP structure [VDS]","base.vds_iscsi_portalgroup_prop","vds/VDS_ISCSI_PORTALGROUP_PROP","vdshwprv/VDS_ISCSI_PORTALGROUP_PROP"]
old-location: base\vds_iscsi_portalgroup_prop.htm
tech.root: base
ms.assetid: 82f891a2-432b-4503-8b5a-a79bea800525
ms.date: 08/05/2022
ms.keywords: '*PVDS_ISCSI_PORTALGROUP_PROP, VDS_ISCSI_PORTALGROUP_PROP, VDS_ISCSI_PORTALGROUP_PROP structure [VDS], base.vds_iscsi_portalgroup_prop, vds/VDS_ISCSI_PORTALGROUP_PROP, vdshwprv/VDS_ISCSI_PORTALGROUP_PROP'
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
req.typenames: VDS_ISCSI_PORTALGROUP_PROP, *PVDS_ISCSI_PORTALGROUP_PROP
req.redist: VDS 1.1
ms.custom: 19H1
f1_keywords:
 - _VDS_ISCSI_PORTALGROUP_PROP
 - vds/_VDS_ISCSI_PORTALGROUP_PROP
 - PVDS_ISCSI_PORTALGROUP_PROP
 - vds/PVDS_ISCSI_PORTALGROUP_PROP
 - VDS_ISCSI_PORTALGROUP_PROP
 - vds/VDS_ISCSI_PORTALGROUP_PROP
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
 - VDS_ISCSI_PORTALGROUP_PROP
---

# VDS_ISCSI_PORTALGROUP_PROP structure


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Defines the properties of an iSCSI portal group.

## -struct-fields

### -field id

The <a href="/windows/desktop/VDS/vds-data-types">VDS_OBJECT_ID</a> assigned to the portal group.

### -field tag

The portal group tag that is assigned by the provider to the portal group. For more information about portal group tags, see the iSCSI specification at <a href="https://www.ietf.org/rfc/rfc3720.txt">https://go.microsoft.com/fwlink/p/?linkid=158752</a>.

## -see-also

<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsiscsiportalgroup-getproperties">IVdsIscsiPortalGroup::GetProperties</a>
