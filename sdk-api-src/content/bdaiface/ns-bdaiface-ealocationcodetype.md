---
UID: NS:bdaiface.EALocationCodeType
title: EALocationCodeType (bdaiface.h)
description: The EALocationCodeType structure defines an Emergency Alert (EA) location code, as defined in ANSI/SCTE 28.
helpviewer_keywords: ["EALocationCodeType","EALocationCodeType structure [Microsoft TV Technologies]","EALocationCodeTypeStructure","bdaiface_enums/EALocationCodeType","mstv.ealocationcodetype"]
old-location: mstv\ealocationcodetype.htm
tech.root: mstv
ms.assetid: dd705e3a-4125-46db-b33d-d97476096484
ms.date: 12/05/2018
ms.keywords: EALocationCodeType, EALocationCodeType structure [Microsoft TV Technologies], EALocationCodeTypeStructure, bdaiface_enums/EALocationCodeType, mstv.ealocationcodetype
req.header: bdaiface.h
req.include-header: Bdaiface.h
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: EALocationCodeType
req.redist: 
ms.custom: 19H1
f1_keywords:
 - EALocationCodeType
 - bdaiface/EALocationCodeType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - bdaiface_enums.h
api_name:
 - EALocationCodeType
---

# EALocationCodeType structure


## -description

The EALocationCodeType structure defines an Emergency Alert (EA) location code, as defined in ANSI/SCTE 28.

## -struct-fields

### -field LocationCodeScheme

Identifies the standard that shall be used to interpret the other members of this structure. Currently this value must be SCTE_18, meaning SCTE 18, "Emergency Alert Message for Cable."

### -field state_code

Contains the state_code field.

### -field county_subdivision

Contains the county_subdivision field.

### -field county_code

Contains the county_code field.

## -see-also

<a href="/previous-versions/windows/desktop/mstv/bda-structures">BDA Structures</a>