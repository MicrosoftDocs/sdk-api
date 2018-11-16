---
UID: NF:ntdsapi.DsFreeSchemaGuidMapW
title: DsFreeSchemaGuidMapW function
author: windows-sdk-content
description: Frees memory that the DsMapSchemaGuids function has allocated for a DS_SCHEMA_GUID_MAP structure.
old-location: ad\dsfreeschemaguidmap.htm
tech.root: ad
ms.assetid: 54d6acb9-5602-4996-a483-08534143bc0a
ms.author: windowssdkdev
ms.date: 11/14/2018
ms.keywords: DsFreeSchemaGuidMap, DsFreeSchemaGuidMap function [Active Directory], DsFreeSchemaGuidMapA, DsFreeSchemaGuidMapW, _glines_dsfreeschemaguidmap, ad.dsfreeschemaguidmap, ntdsapi/DsFreeSchemaGuidMap, ntdsapi/DsFreeSchemaGuidMapA, ntdsapi/DsFreeSchemaGuidMapW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- DsFreeSchemaGuidMapW
: 
---

# DsFreeSchemaGuidMapW function


## -description


The <b>DsFreeSchemaGuidMap</b> function frees memory that the 
<a href="https://msdn.microsoft.com/439fff20-51eb-490d-a330-61d07f79c436">DsMapSchemaGuids</a> function has allocated for a 
<a href="https://msdn.microsoft.com/8128f511-ebdc-479d-b99c-ed210c72d151">DS_SCHEMA_GUID_MAP</a> structure.


## -parameters




### -param pGuidMap [in]

Pointer to a <a href="https://msdn.microsoft.com/8128f511-ebdc-479d-b99c-ed210c72d151">DS_SCHEMA_GUID_MAP</a> structure to deallocate.


## -returns



This function does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/8128f511-ebdc-479d-b99c-ed210c72d151">DS_SCHEMA_GUID_MAP</a>



<a href="https://msdn.microsoft.com/a92783c2-ffb8-473e-8484-1c05ca5453ff">Domain Controller and Replication Management Functions</a>



<a href="https://msdn.microsoft.com/439fff20-51eb-490d-a330-61d07f79c436">DsMapSchemaGuids</a>
 

 

