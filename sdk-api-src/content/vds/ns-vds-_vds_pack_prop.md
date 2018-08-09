---
UID: NS:vds._VDS_PACK_PROP
title: "_VDS_PACK_PROP"
author: windows-sdk-content
description: Defines the properties of a pack object.
old-location: base\vds_pack_prop.htm
old-project: vds
ms.assetid: 5d04bf6c-fda2-4b95-a8bb-907e64267f30
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: "*PVDS_PACK_PROP, PVDS_PACK_PROP, PVDS_PACK_PROP structure pointer [VDS], VDS_PACK_PROP, VDS_PACK_PROP structure [VDS], _VDS_PACK_PROP, base.vds_pack_prop, vds/PVDS_PACK_PROP, vds/_VDS_PACK_PROP"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: VDS_PACK_PROP, *PVDS_PACK_PROP
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Vds.h
api_name:
 - VDS_PACK_PROP
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# _VDS_PACK_PROP structure


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Defines the properties of a pack object.


## -struct-fields




### -field id

The GUID of the pack object.


### -field pwszName

A string representing the pack name. Packs managed by the basic provider have no name.


### -field status

The pack status enumerated by <a href="https://msdn.microsoft.com/a83d01e6-1173-410c-b880-3bc957d3f7e9">VDS_PACK_STATUS</a>.


### -field ulFlags

The pack flags enumerated by <a href="https://msdn.microsoft.com/65b7e65d-5d20-49ff-af35-bd3529f5c858">VDS_PACK_FLAG</a>.


## -remarks



The <a href="https://msdn.microsoft.com/0793642c-1905-470c-a69f-8bf5f8bbe90d">IVdsPack::GetProperties</a>method returns this structure to report the property details of a pack object.




## -see-also




<a href="https://msdn.microsoft.com/0793642c-1905-470c-a69f-8bf5f8bbe90d">IVdsPack::GetProperties</a>



<a href="https://msdn.microsoft.com/6a13f5eb-0fa1-48e2-a112-b2254ca28423">VDS Structures</a>



<a href="https://msdn.microsoft.com/65b7e65d-5d20-49ff-af35-bd3529f5c858">VDS_PACK_FLAG</a>



<a href="https://msdn.microsoft.com/a83d01e6-1173-410c-b880-3bc957d3f7e9">VDS_PACK_STATUS</a>
 

 

