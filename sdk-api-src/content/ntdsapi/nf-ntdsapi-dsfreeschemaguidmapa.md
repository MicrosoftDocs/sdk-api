---
UID: NF:ntdsapi.DsFreeSchemaGuidMapA
title: DsFreeSchemaGuidMapA function (ntdsapi.h)
description: Frees memory that the DsMapSchemaGuids function has allocated for a DS_SCHEMA_GUID_MAP structure. (ANSI)
helpviewer_keywords: ["DsFreeSchemaGuidMapA", "ntdsapi/DsFreeSchemaGuidMapA"]
old-location: ad\dsfreeschemaguidmap.htm
tech.root: ad
ms.assetid: 54d6acb9-5602-4996-a483-08534143bc0a
ms.date: 12/05/2018
ms.keywords: DsFreeSchemaGuidMap, DsFreeSchemaGuidMap function [Active Directory], DsFreeSchemaGuidMapA, DsFreeSchemaGuidMapW, _glines_dsfreeschemaguidmap, ad.dsfreeschemaguidmap, ntdsapi/DsFreeSchemaGuidMap, ntdsapi/DsFreeSchemaGuidMapA, ntdsapi/DsFreeSchemaGuidMapW
req.header: ntdsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: DsFreeSchemaGuidMapW (Unicode) and DsFreeSchemaGuidMapA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Ntdsapi.lib
req.dll: Ntdsapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DsFreeSchemaGuidMapA
 - ntdsapi/DsFreeSchemaGuidMapA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ntdsapi.dll
api_name:
 - DsFreeSchemaGuidMap
 - DsFreeSchemaGuidMapA
 - DsFreeSchemaGuidMapW
---

# DsFreeSchemaGuidMapA function


## -description

The <b>DsFreeSchemaGuidMap</b> function frees memory that the 
<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsmapschemaguidsa">DsMapSchemaGuids</a> function has allocated for a 
<a href="/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_schema_guid_mapa">DS_SCHEMA_GUID_MAP</a> structure.

## -parameters

### -param pGuidMap [in]

Pointer to a <a href="/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_schema_guid_mapa">DS_SCHEMA_GUID_MAP</a> structure to deallocate.

## -returns

This function does not return a value.

## -see-also

<a href="/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_schema_guid_mapa">DS_SCHEMA_GUID_MAP</a>



<a href="/windows/desktop/AD/dc-and-replication-management-functions">Domain Controller and Replication Management Functions</a>



<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsmapschemaguidsa">DsMapSchemaGuids</a>

## -remarks

> [!NOTE]
> The ntdsapi.h header defines DsFreeSchemaGuidMap as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
