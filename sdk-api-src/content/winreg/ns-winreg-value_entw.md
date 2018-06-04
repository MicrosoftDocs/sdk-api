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

# value_entW structure


## -description


Contains information about a registry value. The 
<a href="https://msdn.microsoft.com/e718534a-6e68-40f5-9cdd-170ce9b5e6e5">RegQueryMultipleValues</a> function uses this structure.


## -struct-fields




### -field ve_valuename

The name of the value to be retrieved. Be sure to set this member before calling 
<a href="https://msdn.microsoft.com/e718534a-6e68-40f5-9cdd-170ce9b5e6e5">RegQueryMultipleValues</a>.


### -field ve_valuelen

The size of the data pointed to by <b>ve_valueptr</b>, in bytes.


### -field ve_valueptr

A pointer to the data for the value entry. This is a pointer to the value's data returned in the <b>lpValueBuf</b> buffer filled in by 
<a href="https://msdn.microsoft.com/e718534a-6e68-40f5-9cdd-170ce9b5e6e5">RegQueryMultipleValues</a>.


### -field ve_type

The type of data pointed to by <b>ve_valueptr</b>. For a list of the possible types, see 
<a href="https://msdn.microsoft.com/5fd828d6-4d62-4823-a2f1-15782b5cd28c">Registry Value Types</a>.


## -see-also




<a href="https://msdn.microsoft.com/e718534a-6e68-40f5-9cdd-170ce9b5e6e5">RegQueryMultipleValues</a>
 

 

