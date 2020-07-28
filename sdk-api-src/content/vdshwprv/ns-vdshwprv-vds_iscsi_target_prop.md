---
UID: NS:vdshwprv._VDS_ISCSI_TARGET_PROP
title: VDS_ISCSI_TARGET_PROP (vdshwprv.h)
description: Defines the properties of an iSCSI target.
helpviewer_keywords: ["*PVDS_ISCSI_TARGET_PROP","VDS_ISCSI_TARGET_PROP","VDS_ISCSI_TARGET_PROP structure [VDS]","base.vds_iscsi_target_prop","vds/VDS_ISCSI_TARGET_PROP","vdshwprv/VDS_ISCSI_TARGET_PROP"]
old-location: base\vds_iscsi_target_prop.htm
tech.root: base
ms.assetid: ca92c9e8-4d15-4b3c-8420-3eac18a7c2f5
ms.date: 12/05/2018
ms.keywords: '*PVDS_ISCSI_TARGET_PROP, VDS_ISCSI_TARGET_PROP, VDS_ISCSI_TARGET_PROP structure [VDS], base.vds_iscsi_target_prop, vds/VDS_ISCSI_TARGET_PROP, vdshwprv/VDS_ISCSI_TARGET_PROP'
f1_keywords:
- vdshwprv/VDS_ISCSI_TARGET_PROP
dev_langs:
- c++
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
- VDS_ISCSI_TARGET_PROP
targetos: Windows
req.typenames: VDS_ISCSI_TARGET_PROP, *PVDS_ISCSI_TARGET_PROP
req.redist: VDS 1.1
ms.custom: 19H1
---

# VDS_ISCSI_TARGET_PROP structure


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://docs.microsoft.com/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Defines the properties of an iSCSI target.


## -struct-fields




### -field id

The <b>VDS_OBJECT_ID</b> of the target.


### -field pwszIscsiName

A null-terminated, human-readable string that is the iSCSI name of the target.


### -field pwszFriendlyName

A null-terminated, human-readable string that is the friendly name of the target. This corresponds to the 
     iSCSI alias.


### -field bChapEnabled

If <b>TRUE</b>, a CHAP shared secret is required to login to this target.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsiscsitarget-getproperties">IVdsIscsiTarget::GetProperties</a>
 

 

