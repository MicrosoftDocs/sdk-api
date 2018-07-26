---
UID: NS:ntdsapi.DS_SCHEMA_GUID_MAPA
title: DS_SCHEMA_GUID_MAPA
author: windows-sdk-content
description: Contains the results of a call to DsMapSchemaGuids.
old-location: ad\ds_schema_guid_map.htm
old-project: ad
ms.assetid: 8128f511-ebdc-479d-b99c-ed210c72d151
ms.author: windowssdkdev
ms.date: 07/20/2018
ms.keywords: "*PDS_SCHEMA_GUID_MAPA, DS_SCHEMA_GUID_ATTR, DS_SCHEMA_GUID_ATTR_SET, DS_SCHEMA_GUID_CLASS, DS_SCHEMA_GUID_CONTROL_RIGHT, DS_SCHEMA_GUID_MAP, DS_SCHEMA_GUID_MAP structure [Active Directory], DS_SCHEMA_GUID_MAPA, DS_SCHEMA_GUID_MAPW, DS_SCHEMA_GUID_NOT_FOUND, PDS_SCHEMA_GUID_MAP, PDS_SCHEMA_GUID_MAP structure pointer [Active Directory], _glines_ds_schema_guid_map, ad.ds__schema__guid__map, ad.ds_schema_guid_map, ntdsapi/DS_SCHEMA_GUID_MAP, ntdsapi/DS_SCHEMA_GUID_MAPA, ntdsapi/DS_SCHEMA_GUID_MAPW, ntdsapi/PDS_SCHEMA_GUID_MAP"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: ntdsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: DS_SCHEMA_GUID_MAPW (Unicode) and DS_SCHEMA_GUID_MAPA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: DS_SCHEMA_GUID_MAPA, *PDS_SCHEMA_GUID_MAPA
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ntdsapi.h
api_name:
 - DS_SCHEMA_GUID_MAP
 - DS_SCHEMA_GUID_MAPA
 - DS_SCHEMA_GUID_MAPW
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
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
 

 

