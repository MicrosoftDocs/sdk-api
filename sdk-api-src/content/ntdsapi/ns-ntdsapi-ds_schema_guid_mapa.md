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

# DS_SCHEMA_GUID_MAPA structure


## -description


The <b>DS_SCHEMA_GUID_MAP</b> structure contains the results of a call to 
<a href="https://msdn.microsoft.com/439fff20-51eb-490d-a330-61d07f79c436">DsMapSchemaGuids</a>. If <a href="https://msdn.microsoft.com/439fff20-51eb-490d-a330-61d07f79c436">DsMapSchemaGuids</a> succeeds in mapping a GUID, <b>DS_SCHEMA_GUID_MAP</b> contains both the GUID and a display name for the object to which the GUID refers.


## -struct-fields




### -field guid


<a href="https://msdn.microsoft.com/library/windows/hardware/dn922935">GUID</a> structure that specifies the object GUID.


### -field guidType

Indicates the type of GUID mapped by <a href="https://msdn.microsoft.com/439fff20-51eb-490d-a330-61d07f79c436">DsMapSchemaGuids</a>.



#### DS_SCHEMA_GUID_ATTR

The GUID identifies a property.



#### DS_SCHEMA_GUID_ATTR_SET

The GUID identifies a property set.



#### DS_SCHEMA_GUID_CLASS

The GUID identifies a type of object.



#### DS_SCHEMA_GUID_CONTROL_RIGHT

The GUID identifies an extended access right.



#### DS_SCHEMA_GUID_NOT_FOUND

The GUID cannot be found in the directory service schema.


### -field pName.string

 


### -field pName.unique

 


### -field pName

Pointer to a null-terminated string value that specifies the display name associated with the GUID. This value may be <b>NULL</b> if <a href="https://msdn.microsoft.com/439fff20-51eb-490d-a330-61d07f79c436">DsMapSchemaGuids</a> was unable to map the GUID to a display name.


## -see-also




<a href="https://msdn.microsoft.com/42b20d3b-1799-4f5f-b74e-fe9284dd8ac3">Domain Controller and Replication Management Structures</a>



<a href="https://msdn.microsoft.com/54d6acb9-5602-4996-a483-08534143bc0a">DsFreeSchemaGuidMap</a>



<a href="https://msdn.microsoft.com/439fff20-51eb-490d-a330-61d07f79c436">DsMapSchemaGuids</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn922935">GUID</a>
 

 

