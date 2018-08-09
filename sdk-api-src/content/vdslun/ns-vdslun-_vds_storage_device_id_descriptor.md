---
UID: NS:vdslun._VDS_STORAGE_DEVICE_ID_DESCRIPTOR
title: "_VDS_STORAGE_DEVICE_ID_DESCRIPTOR"
author: windows-sdk-content
description: Defines one or more storage identifiers for a storage device (typically an instance, as opposed to a class, of device).
old-location: base\vds_storage_device_id_descriptor.htm
old-project: vds
ms.assetid: 88fe83cb-6d3c-40bd-a5ce-71771d2e7511
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: VDS_STORAGE_DEVICE_ID_DESCRIPTOR, VDS_STORAGE_DEVICE_ID_DESCRIPTOR structure [VDS], _VDS_STORAGE_DEVICE_ID_DESCRIPTOR, base.vds_storage_device_id_descriptor, vdslun/_VDS_STORAGE_DEVICE_ID_DESCRIPTOR
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: VDS_STORAGE_DEVICE_ID_DESCRIPTOR
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
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# _VDS_STORAGE_DEVICE_ID_DESCRIPTOR structure


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Defines one or more storage identifiers for a storage device (typically an instance, as opposed to a 
   class, of device).
  


## -struct-fields




### -field m_version

The version of this structure.


### -field m_cIdentifiers

The number of identifiers specified in <b>m_rgIdentifiers</b>.


### -field m_rgIdentifiers

Pointer to <a href="https://msdn.microsoft.com/8cc8b6d9-e189-44af-9f2b-2222b2eb0749">VDS_STORAGE_IDENTIFIER</a> structure.
     


## -remarks



Storage devices can have multiple identifiers, and each of these identifiers can have a different code set and 
    type. The <a href="https://msdn.microsoft.com/6ad7ec27-add1-4f1e-aa01-6f43c75b7ad9">VDS_LUN_INFORMATION</a> structure includes 
    this structure as a member to specify the storage device identifiers of a LUN.




## -see-also




<a href="https://msdn.microsoft.com/6a13f5eb-0fa1-48e2-a112-b2254ca28423">VDS Structures</a>



<a href="https://msdn.microsoft.com/6ad7ec27-add1-4f1e-aa01-6f43c75b7ad9">VDS_LUN_INFORMATION</a>



<a href="https://msdn.microsoft.com/8cc8b6d9-e189-44af-9f2b-2222b2eb0749">VDS_STORAGE_IDENTIFIER</a>
 

 

