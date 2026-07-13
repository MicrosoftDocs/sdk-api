---
UID: NF:ntdsapi.DsMapSchemaGuidsW
title: DsMapSchemaGuidsW function (ntdsapi.h)
description: Converts GUIDs of directory service schema objects to their display names. (Unicode)
helpviewer_keywords: ["DsMapSchemaGuids", "DsMapSchemaGuids function [Active Directory]", "DsMapSchemaGuidsW", "_glines_dsmapschemaguids", "ad.dsmapschemaguids", "ntdsapi/DsMapSchemaGuids", "ntdsapi/DsMapSchemaGuidsW"]
old-location: ad\dsmapschemaguids.htm
tech.root: ad
ms.assetid: 439fff20-51eb-490d-a330-61d07f79c436
ms.date: 12/05/2018
ms.keywords: DsMapSchemaGuids, DsMapSchemaGuids function [Active Directory], DsMapSchemaGuidsA, DsMapSchemaGuidsW, _glines_dsmapschemaguids, ad.dsmapschemaguids, ntdsapi/DsMapSchemaGuids, ntdsapi/DsMapSchemaGuidsA, ntdsapi/DsMapSchemaGuidsW
req.header: ntdsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: DsMapSchemaGuidsW (Unicode) and DsMapSchemaGuidsA (ANSI)
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
 - DsMapSchemaGuidsW
 - ntdsapi/DsMapSchemaGuidsW
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
 - DsMapSchemaGuids
 - DsMapSchemaGuidsA
 - DsMapSchemaGuidsW
---

# DsMapSchemaGuidsW function


## -description

The <b>DsMapSchemaGuids</b> function converts GUIDs of directory service schema objects to their display names.

## -parameters

### -param hDs [in]

Contains a directory service handle obtained from either the 
<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsbinda">DSBind</a> or 
<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsbindwithcreda">DSBindWithCred</a> function.

### -param cGuids [in]

Indicates the number of elements in <i>rGuids</i>.

### -param rGuids [in]

Pointer to an array of <b>GUID</b> values for the objects to be mapped.

### -param ppGuidMap [out]

Pointer to a variable that receives a pointer to an array of 
<a href="/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_schema_guid_mapa">DS_SCHEMA_GUID_MAP</a> structures that contain the display names of the objects in <i>rGuids</i>. This array must be deallocated using 
<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsfreeschemaguidmapa">DsFreeSchemaGuidMap</a>.

## -returns

Returns a standard error code that includes the following values.

## -see-also

<a href="/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_schema_guid_mapa">DS_SCHEMA_GUID_MAP</a>



<a href="/windows/desktop/AD/dc-and-replication-management-functions">Domain Controller and Replication Management Functions</a>



<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsfreeschemaguidmapa">DsFreeSchemaGuidMap</a>

## -remarks

> [!NOTE]
> The ntdsapi.h header defines DsMapSchemaGuids as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
