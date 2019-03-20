---
UID: NS:vds._VDS_ISCSI_INITIATOR_ADAPTER_PROP
title: VDS_ISCSI_INITIATOR_ADAPTER_PROP (vds.h)
author: windows-sdk-content
description: Defines the properties of an iSCSI initiator adapter.
old-location: base\vds_iscsi_initiator_adapter_prop.htm
tech.root: VDS
ms.assetid: cfcc7c7a-d135-4404-8f67-64e43a425669
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: VDS_ISCSI_INITIATOR_ADAPTER_PROP, VDS_ISCSI_INITIATOR_ADAPTER_PROP structure [VDS], _VDS_ISCSI_INITIATOR_ADAPTER_PROP, base.vds_iscsi_initiator_adapter_prop, vds/VDS_ISCSI_INITIATOR_ADAPTER_PROP, vdshwprv/VDS_ISCSI_INITIATOR_ADAPTER_PROP
ms.topic: struct
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
product: Windows
targetos: Windows
req.typenames: VDS_ISCSI_INITIATOR_ADAPTER_PROP
req.redist: VDS 1.1
---

# VDS_ISCSI_INITIATOR_ADAPTER_PROP structure


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Defines the properties of an iSCSI initiator adapter.


## -struct-fields




### -field id

The <b>VDS_OBJECT_ID</b> assigned to the initiator adapter.


### -field pwszName

A null-terminated, human-readable string that is the name of the initiator adapter.


## -see-also




<a href="https://msdn.microsoft.com/9442e182-bc2e-47dd-9ddc-aa1a618a5563">IVdsIscsiInitiatorAdapter::GetProperties</a>
 

 

