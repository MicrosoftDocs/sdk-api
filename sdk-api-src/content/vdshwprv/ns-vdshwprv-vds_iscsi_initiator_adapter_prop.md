---
UID: NS:vdshwprv._VDS_ISCSI_INITIATOR_ADAPTER_PROP
title: VDS_ISCSI_INITIATOR_ADAPTER_PROP (vdshwprv.h)
description: The VDS_ISCSI_INITIATOR_ADAPTER_PROP structure (vdshwprv.h) defines the properties of an iSCSI initiator adapter.
helpviewer_keywords: ["VDS_ISCSI_INITIATOR_ADAPTER_PROP","VDS_ISCSI_INITIATOR_ADAPTER_PROP structure [VDS]","_VDS_ISCSI_INITIATOR_ADAPTER_PROP","base.vds_iscsi_initiator_adapter_prop","vds/VDS_ISCSI_INITIATOR_ADAPTER_PROP","vdshwprv/VDS_ISCSI_INITIATOR_ADAPTER_PROP"]
old-location: base\vds_iscsi_initiator_adapter_prop.htm
tech.root: base
ms.assetid: cfcc7c7a-d135-4404-8f67-64e43a425669
ms.date: 08/08/2022
ms.keywords: VDS_ISCSI_INITIATOR_ADAPTER_PROP, VDS_ISCSI_INITIATOR_ADAPTER_PROP structure [VDS], _VDS_ISCSI_INITIATOR_ADAPTER_PROP, base.vds_iscsi_initiator_adapter_prop, vds/VDS_ISCSI_INITIATOR_ADAPTER_PROP, vdshwprv/VDS_ISCSI_INITIATOR_ADAPTER_PROP
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
req.typenames: VDS_ISCSI_INITIATOR_ADAPTER_PROP
req.redist: VDS 1.1
ms.custom: 19H1
f1_keywords:
 - _VDS_ISCSI_INITIATOR_ADAPTER_PROP
 - vdshwprv/_VDS_ISCSI_INITIATOR_ADAPTER_PROP
 - VDS_ISCSI_INITIATOR_ADAPTER_PROP
 - vdshwprv/VDS_ISCSI_INITIATOR_ADAPTER_PROP
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
 - VDS_ISCSI_INITIATOR_ADAPTER_PROP
---

# VDS_ISCSI_INITIATOR_ADAPTER_PROP structure


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Defines the properties of an iSCSI initiator adapter.

## -struct-fields

### -field id

The <b>VDS_OBJECT_ID</b> assigned to the initiator adapter.

### -field pwszName

A null-terminated, human-readable string that is the name of the initiator adapter.

## -see-also

<a href="/windows/desktop/api/vds/nf-vds-ivdsiscsiinitiatoradapter-getproperties">IVdsIscsiInitiatorAdapter::GetProperties</a>
