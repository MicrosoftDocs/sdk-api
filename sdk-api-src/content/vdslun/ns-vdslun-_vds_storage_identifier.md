---
UID: NS:vdslun._VDS_STORAGE_IDENTIFIER
title: "_VDS_STORAGE_IDENTIFIER"
author: windows-sdk-content
description: Defines a storage device using a particular code set and type.
old-location: base\vds_storage_identifier.htm
old-project: VDS
ms.assetid: 8cc8b6d9-e189-44af-9f2b-2222b2eb0749
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: VDS_STORAGE_IDENTIFIER, VDS_STORAGE_IDENTIFIER structure [VDS], _VDS_STORAGE_IDENTIFIER, base.vds_storage_identifier, vdslun/_VDS_STORAGE_IDENTIFIER
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
req.typenames: VDS_STORAGE_IDENTIFIER
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - VdsLun.h
api_name:
 - VDS_STORAGE_IDENTIFIER
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# _VDS_STORAGE_IDENTIFIER structure


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Defines a 
   storage device using a particular code set and type.


## -struct-fields




### -field m_CodeSet


      The encoding type of <b>m_rgbIdentifier</b> enumerated by 
      <a href="https://msdn.microsoft.com/6b4a3282-dc0c-4974-8c4c-777a28fb9005">VDS_STORAGE_IDENTIFIER_CODE_SET</a>.


### -field m_Type


      The type of <b>m_rgbIdentifier</b> enumerated by 
      <a href="https://msdn.microsoft.com/396ca6c1-fae3-4584-97c9-2c4dfbc170d5">VDS_STORAGE_IDENTIFIER_TYPE</a>.


### -field m_cbIdentifier

The size of the <b>m_rgbIdentifier</b> array, in bytes.


### -field m_rgbIdentifier

Pointer to the identifier data.


## -remarks




    The <a href="https://msdn.microsoft.com/88fe83cb-6d3c-40bd-a5ce-71771d2e7511">VDS_STORAGE_DEVICE_ID_DESCRIPTOR</a> 
    structure includes this structure as a member to specify a particular storage device identifier for a LUN.




## -see-also




<a href="https://msdn.microsoft.com/6a13f5eb-0fa1-48e2-a112-b2254ca28423">VDS Structures</a>



<a href="https://msdn.microsoft.com/88fe83cb-6d3c-40bd-a5ce-71771d2e7511">VDS_STORAGE_DEVICE_ID_DESCRIPTOR</a>



<a href="https://msdn.microsoft.com/6b4a3282-dc0c-4974-8c4c-777a28fb9005">VDS_STORAGE_IDENTIFIER_CODE_SET</a>



<a href="https://msdn.microsoft.com/396ca6c1-fae3-4584-97c9-2c4dfbc170d5">VDS_STORAGE_IDENTIFIER_TYPE</a>
 

 

