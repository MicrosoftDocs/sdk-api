---
UID: NS:vds._VDS_SERVICE_PROP
title: VDS_SERVICE_PROP (vds.h)
description: Defines the properties of the service object.
helpviewer_keywords: ["VDS_SERVICE_PROP","VDS_SERVICE_PROP structure [VDS]","base.vds_service_prop","vds/_VDS_SERVICE_PROP"]
old-location: base\vds_service_prop.htm
tech.root: base
ms.assetid: 9029ebbd-f05d-4317-913d-58c8a0a62886
ms.date: 12/05/2018
ms.keywords: VDS_SERVICE_PROP, VDS_SERVICE_PROP structure [VDS], base.vds_service_prop, vds/_VDS_SERVICE_PROP
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
req.typenames: VDS_SERVICE_PROP
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _VDS_SERVICE_PROP
 - vds/_VDS_SERVICE_PROP
 - VDS_SERVICE_PROP
 - vds/VDS_SERVICE_PROP
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
 - VDS_SERVICE_PROP
---

# VDS_SERVICE_PROP structure


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Defines the properties of the <a href="/windows/desktop/VDS/startup-and-service-objects">service object</a>.

## -struct-fields

### -field pwszVersion

The version of VDS; a zero-terminated, human-readable string.

### -field ulFlags

A bitmask of <a href="/windows/desktop/api/vds/ne-vds-vds_service_flag">VDS_SERVICE_FLAG</a> enumeration values that describe the service.

## -remarks

 The <a href="/windows/desktop/api/vds/nf-vds-ivdsservice-getproperties">IVdsService::GetProperties</a> method returns this structure to report the properties of the <a href="/windows/desktop/VDS/startup-and-service-objects">service object</a>.

## -see-also

<a href="/windows/desktop/api/vds/nf-vds-ivdsservice-getproperties">IVdsService::GetProperties</a>



<a href="/windows/desktop/VDS/vds-structures">VDS Structures</a>