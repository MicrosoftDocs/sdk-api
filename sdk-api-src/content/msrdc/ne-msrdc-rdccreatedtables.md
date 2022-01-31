---
UID: NE:msrdc.__MIDL___MIDL_itf_msrdc_0000_0000_0009
title: RdcCreatedTables (msrdc.h)
description: Defines values that describe the state of the similarity traits table, similarity file ID table, or both.
helpviewer_keywords: ["RDCTABLE_Existing","RDCTABLE_InvalidOrUnknown","RDCTABLE_New","RdcCreatedTables","RdcCreatedTables enumeration [Remote Differential Compression]","fs.rdccreatedtables","msrdc/RDCTABLE_Existing","msrdc/RDCTABLE_InvalidOrUnknown","msrdc/RDCTABLE_New","msrdc/RdcCreatedTables","rdc.rdccreatedtables"]
old-location: rdc\rdccreatedtables.htm
tech.root: rdc
ms.assetid: f46dd0f0-22b0-41fb-a7c2-29d1b4514f7e
ms.date: 12/05/2018
ms.keywords: RDCTABLE_Existing, RDCTABLE_InvalidOrUnknown, RDCTABLE_New, RdcCreatedTables, RdcCreatedTables enumeration [Remote Differential Compression], fs.rdccreatedtables, msrdc/RDCTABLE_Existing, msrdc/RDCTABLE_InvalidOrUnknown, msrdc/RDCTABLE_New, msrdc/RdcCreatedTables, rdc.rdccreatedtables
req.header: msrdc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: MsRdc.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: RdcCreatedTables
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_msrdc_0000_0000_0009
 - msrdc/__MIDL___MIDL_itf_msrdc_0000_0000_0009
 - RdcCreatedTables
 - msrdc/RdcCreatedTables
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - MsRdc.h
api_name:
 - RdcCreatedTables
---

# RdcCreatedTables enumeration


## -description

Defines values that describe the state of the similarity traits table, similarity file ID table, or both.

## -enum-fields

### -field RDCTABLE_InvalidOrUnknown:0

The table contains data that is not valid.

### -field RDCTABLE_Existing

The table is an existing table.

### -field RDCTABLE_New

The table is a new table.

## -see-also

<a href="/previous-versions/windows/desktop/api/msrdc/nf-msrdc-isimilarity-createtable">ISimilarity::CreateTable</a>



<a href="/previous-versions/windows/desktop/api/msrdc/nf-msrdc-isimilarityfileidtable-createtable">ISimilarityFileIdTable::CreateTable</a>



<a href="/previous-versions/windows/desktop/api/msrdc/nf-msrdc-isimilaritytraitstable-createtable">ISimilarityTraitsTable::CreateTable</a>
