---
UID: NS:vds._VDS_POOL_CUSTOM_ATTRIBUTES
title: VDS_POOL_CUSTOM_ATTRIBUTES (vds.h)
description: The VDS_POOL_CUSTOM_ATTRIBUTES structure (vds.h) defines a custom attribute of a storage pool.  
helpviewer_keywords: ["*PVDS_POOL_CUSTOM_ATTRIBUTES","PVDS_POOL_CUSTOM_ATTRIBUTES","PVDS_POOL_CUSTOM_ATTRIBUTES structure pointer","VDS_POOL_CUSTOM_ATTRIBUTES","VDS_POOL_CUSTOM_ATTRIBUTES structure","base.vds_pool_custom_attributes","vds/PVDS_POOL_CUSTOM_ATTRIBUTES","vds/VDS_POOL_CUSTOM_ATTRIBUTES","vdshwprv/PVDS_POOL_CUSTOM_ATTRIBUTES","vdshwprv/VDS_POOL_CUSTOM_ATTRIBUTES"]
old-location: base\vds_pool_custom_attributes.htm
tech.root: base
ms.assetid: beea122a-476c-43e0-bb70-2555d4211bf7
ms.date: 08/05/2022
ms.keywords: '*PVDS_POOL_CUSTOM_ATTRIBUTES, PVDS_POOL_CUSTOM_ATTRIBUTES, PVDS_POOL_CUSTOM_ATTRIBUTES structure pointer, VDS_POOL_CUSTOM_ATTRIBUTES, VDS_POOL_CUSTOM_ATTRIBUTES structure, base.vds_pool_custom_attributes, vds/PVDS_POOL_CUSTOM_ATTRIBUTES, vds/VDS_POOL_CUSTOM_ATTRIBUTES, vdshwprv/PVDS_POOL_CUSTOM_ATTRIBUTES, vdshwprv/VDS_POOL_CUSTOM_ATTRIBUTES'
req.header: vds.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: VDS_POOL_CUSTOM_ATTRIBUTES, *PVDS_POOL_CUSTOM_ATTRIBUTES
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _VDS_POOL_CUSTOM_ATTRIBUTES
 - vds/_VDS_POOL_CUSTOM_ATTRIBUTES
 - PVDS_POOL_CUSTOM_ATTRIBUTES
 - vds/PVDS_POOL_CUSTOM_ATTRIBUTES
 - VDS_POOL_CUSTOM_ATTRIBUTES
 - vds/VDS_POOL_CUSTOM_ATTRIBUTES
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
 - VDS_POOL_CUSTOM_ATTRIBUTES
---

# VDS_POOL_CUSTOM_ATTRIBUTES structure


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Defines a custom attribute of a <a href="/windows/desktop/VDS/storage-pool-object">storage pool</a>. This structure is used in the <a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_pool_attributes">pPoolCustomAttributes</a> member of the <b>VDS_POOL_ATTRIBUTES</b> structure.

## -struct-fields

### -field pwszName

A string containing the name of the custom attribute.

### -field pwszValue

A string containing the value of the custom attribute.

## -remarks

A custom attribute can be used to indicate, for example, the RAID types that can be created in the storage pool in  cases such as the following:

<ul>
<li>The storage pool supports the creation of LUNs without any RAID type.</li>
<li>The storage pool supports more than one RAID type. This can happen if the storage pool spans more than one subsystem.</li>
</ul>

## -see-also

<a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_pool_attributes">VDS_POOL_ATTRIBUTES</a>
