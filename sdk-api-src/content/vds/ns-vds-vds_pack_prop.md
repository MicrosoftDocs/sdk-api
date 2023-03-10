---
UID: NS:vds._VDS_PACK_PROP
title: VDS_PACK_PROP (vds.h)
description: Defines the properties of a pack object.
helpviewer_keywords: ["*PVDS_PACK_PROP","PVDS_PACK_PROP","PVDS_PACK_PROP structure pointer [VDS]","VDS_PACK_PROP","VDS_PACK_PROP structure [VDS]","base.vds_pack_prop","vds/PVDS_PACK_PROP","vds/_VDS_PACK_PROP"]
old-location: base\vds_pack_prop.htm
tech.root: base
ms.assetid: 5d04bf6c-fda2-4b95-a8bb-907e64267f30
ms.date: 12/05/2018
ms.keywords: '*PVDS_PACK_PROP, PVDS_PACK_PROP, PVDS_PACK_PROP structure pointer [VDS], VDS_PACK_PROP, VDS_PACK_PROP structure [VDS], base.vds_pack_prop, vds/PVDS_PACK_PROP, vds/_VDS_PACK_PROP'
req.header: vds.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: VDS_PACK_PROP, *PVDS_PACK_PROP
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _VDS_PACK_PROP
 - vds/_VDS_PACK_PROP
 - PVDS_PACK_PROP
 - vds/PVDS_PACK_PROP
 - VDS_PACK_PROP
 - vds/VDS_PACK_PROP
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Vds.h
api_name:
 - VDS_PACK_PROP
---

# VDS_PACK_PROP structure


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Defines the properties of a pack object.

## -struct-fields

### -field id

The GUID of the pack object.

### -field pwszName

A string representing the pack name. Packs managed by the basic provider have no name.

### -field status

The pack status enumerated by <a href="/windows/desktop/api/vds/ne-vds-vds_pack_status">VDS_PACK_STATUS</a>.

### -field ulFlags

The pack flags enumerated by <a href="/windows/desktop/api/vds/ne-vds-vds_pack_flag">VDS_PACK_FLAG</a>.

## -remarks

The <a href="/windows/desktop/api/vds/nf-vds-ivdspack-getproperties">IVdsPack::GetProperties</a> method returns this structure to report the property details of a pack object.

## -see-also

<a href="/windows/desktop/api/vds/nf-vds-ivdspack-getproperties">IVdsPack::GetProperties</a>



<a href="/windows/desktop/VDS/vds-structures">VDS Structures</a>



<a href="/windows/desktop/api/vds/ne-vds-vds_pack_flag">VDS_PACK_FLAG</a>



<a href="/windows/desktop/api/vds/ne-vds-vds_pack_status">VDS_PACK_STATUS</a>