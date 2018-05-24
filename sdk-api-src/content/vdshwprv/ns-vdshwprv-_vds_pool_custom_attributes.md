---
UID: NS:vdshwprv._VDS_POOL_CUSTOM_ATTRIBUTES
title: "_VDS_POOL_CUSTOM_ATTRIBUTES"
author: windows-driver-content
description: Defines a custom attribute of a storage pool.
old-location: base\vds_pool_custom_attributes.htm
old-project: VDS
ms.assetid: beea122a-476c-43e0-bb70-2555d4211bf7
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: "*PVDS_POOL_CUSTOM_ATTRIBUTES, PVDS_POOL_CUSTOM_ATTRIBUTES, PVDS_POOL_CUSTOM_ATTRIBUTES structure pointer, VDS_POOL_CUSTOM_ATTRIBUTES, VDS_POOL_CUSTOM_ATTRIBUTES structure, _VDS_POOL_CUSTOM_ATTRIBUTES, base.vds_pool_custom_attributes, vds/PVDS_POOL_CUSTOM_ATTRIBUTES, vds/VDS_POOL_CUSTOM_ATTRIBUTES, vdshwprv/PVDS_POOL_CUSTOM_ATTRIBUTES, vdshwprv/VDS_POOL_CUSTOM_ATTRIBUTES"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: vdshwprv.h
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
req.typenames: VDS_POOL_CUSTOM_ATTRIBUTES, *PVDS_POOL_CUSTOM_ATTRIBUTES
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Vds.h
-	VdsHwPrv.h
api_name:
-	VDS_POOL_CUSTOM_ATTRIBUTES
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# _VDS_POOL_CUSTOM_ATTRIBUTES structure


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Defines a custom attribute of a <a href="https://msdn.microsoft.com/a6104742-3ef9-4570-9728-3e6580953117">storage pool</a>. This structure is used in the <a href="https://msdn.microsoft.com/3dfbd3d9-ec2e-44ac-9d0f-7aa6c530db18">pPoolCustomAttributes</a> member of the <b>VDS_POOL_ATTRIBUTES</b> structure.


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




<a href="https://msdn.microsoft.com/3dfbd3d9-ec2e-44ac-9d0f-7aa6c530db18">VDS_POOL_ATTRIBUTES</a>
 

 

