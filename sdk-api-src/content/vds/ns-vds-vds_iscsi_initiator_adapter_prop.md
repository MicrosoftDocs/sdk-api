---
UID: NS:vds._VDS_ISCSI_INITIATOR_ADAPTER_PROP
title: VDS_ISCSI_INITIATOR_ADAPTER_PROP (vds.h)

description: Defines the properties of an iSCSI initiator adapter.
old-location: base\vds_iscsi_initiator_adapter_prop.htm
tech.root: VDS
ms.assetid: cfcc7c7a-d135-4404-8f67-64e43a425669

ms.date: 12/05/2018
ms.keywords: VDS_ISCSI_INITIATOR_ADAPTER_PROP, VDS_ISCSI_INITIATOR_ADAPTER_PROP structure [VDS], _VDS_ISCSI_INITIATOR_ADAPTER_PROP, base.vds_iscsi_initiator_adapter_prop, vds/VDS_ISCSI_INITIATOR_ADAPTER_PROP, vdshwprv/VDS_ISCSI_INITIATOR_ADAPTER_PROP
ms.topic: struct
f1_keywords: 
 - "vds/VDS_ISCSI_INITIATOR_ADAPTER_PROP"
dev_langs:
 - c++
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
targetos: Windows
req.typenames: VDS_ISCSI_INITIATOR_ADAPTER_PROP
req.redist: VDS 1.1
ms.custom: 19H1
---

# VDS_ISCSI_INITIATOR_ADAPTER_PROP structure


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://docs.microsoft.com/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Defines the properties of an iSCSI initiator adapter.


## -struct-fields




### -field id

The <b>VDS_OBJECT_ID</b> assigned to the initiator adapter.


### -field pwszName

A null-terminated, human-readable string that is the name of the initiator adapter.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsiscsiinitiatoradapter-getproperties">IVdsIscsiInitiatorAdapter::GetProperties</a>
 

 

