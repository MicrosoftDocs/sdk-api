---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

