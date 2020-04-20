---
UID: NS:ntdsapi.__unnamed_struct_11
title: DS_SCHEMA_GUID_MAPA (ntdsapi.h)
description: Contains the results of a call to DsMapSchemaGuids.helpviewer_keywords: ["*PDS_SCHEMA_GUID_MAPA","DS_SCHEMA_GUID_ATTR","DS_SCHEMA_GUID_ATTR_SET","DS_SCHEMA_GUID_CLASS","DS_SCHEMA_GUID_CONTROL_RIGHT","DS_SCHEMA_GUID_MAP","DS_SCHEMA_GUID_MAP structure [Active Directory]","DS_SCHEMA_GUID_MAPA","DS_SCHEMA_GUID_MAPW","DS_SCHEMA_GUID_NOT_FOUND","PDS_SCHEMA_GUID_MAP","PDS_SCHEMA_GUID_MAP structure pointer [Active Directory]","_glines_ds_schema_guid_map","ad.ds__schema__guid__map","ad.ds_schema_guid_map","ntdsapi/DS_SCHEMA_GUID_MAP","ntdsapi/DS_SCHEMA_GUID_MAPA","ntdsapi/DS_SCHEMA_GUID_MAPW","ntdsapi/PDS_SCHEMA_GUID_MAP"]
old-location: ad\ds_schema_guid_map.htm
tech.root: ad
ms.assetid: 8128f511-ebdc-479d-b99c-ed210c72d151
ms.date: 12/05/2018
ms.keywords: '*PDS_SCHEMA_GUID_MAPA, DS_SCHEMA_GUID_ATTR, DS_SCHEMA_GUID_ATTR_SET, DS_SCHEMA_GUID_CLASS, DS_SCHEMA_GUID_CONTROL_RIGHT, DS_SCHEMA_GUID_MAP, DS_SCHEMA_GUID_MAP structure [Active Directory], DS_SCHEMA_GUID_MAPA, DS_SCHEMA_GUID_MAPW, DS_SCHEMA_GUID_NOT_FOUND, PDS_SCHEMA_GUID_MAP, PDS_SCHEMA_GUID_MAP structure pointer [Active Directory], _glines_ds_schema_guid_map, ad.ds__schema__guid__map, ad.ds_schema_guid_map, ntdsapi/DS_SCHEMA_GUID_MAP, ntdsapi/DS_SCHEMA_GUID_MAPA, ntdsapi/DS_SCHEMA_GUID_MAPW, ntdsapi/PDS_SCHEMA_GUID_MAP'
f1_keywords:
- ntdsapi/DS_SCHEMA_GUID_MAP
dev_langs:
- c++
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
req.lib: 
req.dll: 
req.irql: 
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
targetos: Windows
req.typenames: DS_SCHEMA_GUID_MAPA, *PDS_SCHEMA_GUID_MAPA
req.redist: 
ms.custom: 19H1
---

# DS_SCHEMA_GUID_MAPA structure


## -description


The <b>DS_SCHEMA_GUID_MAP</b> structure contains the results of a call to 
<a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/nf-ntdsapi-dsmapschemaguidsa">DsMapSchemaGuids</a>. If <a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/nf-ntdsapi-dsmapschemaguidsa">DsMapSchemaGuids</a> succeeds in mapping a GUID, <b>DS_SCHEMA_GUID_MAP</b> contains both the GUID and a display name for the object to which the GUID refers.


## -struct-fields




### -field guid


<a href="/windows/win32/api/guiddef/ns-guiddef-guid">GUID</a> structure that specifies the object GUID.


### -field guidType

Indicates the type of GUID mapped by <a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/nf-ntdsapi-dsmapschemaguidsa">DsMapSchemaGuids</a>.



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


### -field string

 


### -field unique

 


### -field pName

Pointer to a null-terminated string value that specifies the display name associated with the GUID. This value may be <b>NULL</b> if <a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/nf-ntdsapi-dsmapschemaguidsa">DsMapSchemaGuids</a> was unable to map the GUID to a display name.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/AD/domain-controller-and-replication-management-structures">Domain Controller and Replication Management Structures</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/nf-ntdsapi-dsfreeschemaguidmapa">DsFreeSchemaGuidMap</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/nf-ntdsapi-dsmapschemaguidsa">DsMapSchemaGuids</a>



<a href="/windows/win32/api/guiddef/ns-guiddef-guid">GUID</a>
 

 

