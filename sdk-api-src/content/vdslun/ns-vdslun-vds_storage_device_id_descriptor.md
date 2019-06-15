---
UID: NS:vdslun._VDS_STORAGE_DEVICE_ID_DESCRIPTOR
title: VDS_STORAGE_DEVICE_ID_DESCRIPTOR (vdslun.h)
author: windows-sdk-content
description: Defines one or more storage identifiers for a storage device (typically an instance, as opposed to a class, of device).
old-location: base\vds_storage_device_id_descriptor.htm
tech.root: VDS
ms.assetid: 88fe83cb-6d3c-40bd-a5ce-71771d2e7511
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: VDS_STORAGE_DEVICE_ID_DESCRIPTOR, VDS_STORAGE_DEVICE_ID_DESCRIPTOR structure [VDS], base.vds_storage_device_id_descriptor, vdslun/_VDS_STORAGE_DEVICE_ID_DESCRIPTOR
ms.topic: struct
f1_keywords: ["vdslun/VDS_STORAGE_DEVICE_ID_DESCRIPTOR"]
req.header: vdslun.h
req.include-header: Vds.h, VdsHwPrv.h for hardware providers
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - VdsLun.h
api_name:
 - VDS_STORAGE_DEVICE_ID_DESCRIPTOR
product: Windows
targetos: Windows
req.typenames: VDS_STORAGE_DEVICE_ID_DESCRIPTOR
req.redist: 
ms.custom: 19H1
---

# VDS_STORAGE_DEVICE_ID_DESCRIPTOR structure


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://docs.microsoft.com/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Defines one or more storage identifiers for a storage device (typically an instance, as opposed to a 
   class, of device).
  


## -struct-fields




### -field m_version

The version of this structure.


### -field m_cIdentifiers

The number of identifiers specified in <b>m_rgIdentifiers</b>.


### -field m_rgIdentifiers

Pointer to <a href="https://docs.microsoft.com/windows/desktop/api/vdslun/ns-vdslun-_vds_storage_identifier">VDS_STORAGE_IDENTIFIER</a> structure.
     


## -remarks



Storage devices can have multiple identifiers, and each of these identifiers can have a different code set and 
    type. The <a href="https://docs.microsoft.com/windows/desktop/api/vdslun/ns-vdslun-_vds_lun_information">VDS_LUN_INFORMATION</a> structure includes 
    this structure as a member to specify the storage device identifiers of a LUN.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/VDS/vds-structures">VDS Structures</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vdslun/ns-vdslun-_vds_lun_information">VDS_LUN_INFORMATION</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vdslun/ns-vdslun-_vds_storage_identifier">VDS_STORAGE_IDENTIFIER</a>
 

 

