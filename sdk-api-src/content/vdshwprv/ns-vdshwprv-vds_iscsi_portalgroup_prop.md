---
UID: NS:vdshwprv._VDS_ISCSI_PORTALGROUP_PROP
title: VDS_ISCSI_PORTALGROUP_PROP (vdshwprv.h)
author: windows-sdk-content
description: Defines the properties of an iSCSI portal group.
old-location: base\vds_iscsi_portalgroup_prop.htm
tech.root: VDS
ms.assetid: 82f891a2-432b-4503-8b5a-a79bea800525
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PVDS_ISCSI_PORTALGROUP_PROP, VDS_ISCSI_PORTALGROUP_PROP, VDS_ISCSI_PORTALGROUP_PROP structure [VDS], base.vds_iscsi_portalgroup_prop, vds/VDS_ISCSI_PORTALGROUP_PROP, vdshwprv/VDS_ISCSI_PORTALGROUP_PROP"
ms.topic: struct
f1_keywords: 
 - "vdshwprv/VDS_ISCSI_PORTALGROUP_PROP"
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
product: Windows
targetos: Windows
req.typenames: VDS_ISCSI_PORTALGROUP_PROP, *PVDS_ISCSI_PORTALGROUP_PROP
req.redist: VDS 1.1
ms.custom: 19H1
---

# VDS_ISCSI_PORTALGROUP_PROP structure


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://docs.microsoft.com/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Defines the properties of an iSCSI portal group.


## -struct-fields




### -field id

The <a href="https://docs.microsoft.com/windows/desktop/VDS/vds-data-types">VDS_OBJECT_ID</a> assigned to the portal group.


### -field tag

The portal group tag that is assigned by the provider to the portal group. For more information about portal group tags, see the iSCSI specification at <a href="http://go.microsoft.com/fwlink/p/?linkid=158752">http://go.microsoft.com/fwlink/p/?linkid=158752</a>.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsiscsiportalgroup-getproperties">IVdsIscsiPortalGroup::GetProperties</a>
 

 

