---
UID: NS:tdh._PROVIDER_FIELD_INFOARRAY
title: PROVIDER_FIELD_INFOARRAY (tdh.h)
author: windows-sdk-content
description: Defines metadata information about the requested field.
old-location: etw\provider_field_infoarray_struct.htm
tech.root: ETW
ms.assetid: c3755ca2-7b17-4f86-9ae8-34621f8b8c1b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PPROVIDER_FIELD_INFOARRAY, PROVIDER_FIELD_INFOARRAY, PROVIDER_FIELD_INFOARRAY structure [ETW], etw.provider_field_infoarray_struct, tdh.provider_field_infoarray_struct, tdh/PROVIDER_FIELD_INFOARRAY"
ms.topic: struct
req.header: tdh.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - Tdh.h
api_name:
 - PROVIDER_FIELD_INFOARRAY
product: Windows
targetos: Windows
req.typenames: PROVIDER_FIELD_INFOARRAY
req.redist: 
ms.custom: 19H1
---

# PROVIDER_FIELD_INFOARRAY structure


## -description


Defines metadata information about the requested field.
		
		
	
	


## -struct-fields




### -field NumberOfElements

Number of elements in the <b>FieldInfoArray</b> array.


### -field FieldType

Type of field information in  the <b>FieldInfoArray</b> array. For possible values, see the <a href="https://msdn.microsoft.com/da525556-e42b-41cb-b954-300f378477e5">EVENT_FIELD_TYPE</a> enumeration. 


### -field FieldInfoArray

Array of <a href="https://msdn.microsoft.com/a7c88c25-3acc-42aa-bf2b-bc7651e84f8c">PROVIDER_FIELD_INFO</a> structures that define the field's name, description and value.


## -see-also




<a href="https://msdn.microsoft.com/ab34a433-b641-4408-81d5-c93609204d24">TdhEnumerateProviderFieldInformation</a>



<a href="https://msdn.microsoft.com/ca3c1519-0b86-4bdb-b027-9c662df5466e">TdhQueryProviderFieldInformation</a>
 

 

