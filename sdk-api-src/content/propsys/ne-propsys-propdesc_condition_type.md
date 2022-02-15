---
UID: NE:propsys.PROPDESC_CONDITION_TYPE
title: PROPDESC_CONDITION_TYPE (propsys.h)
description: Describes the condition type to use when displaying the property in the query builder UI in Windows Vista, but not in Windows 7 and later.
helpviewer_keywords: ["PDCOT_BOOLEAN","PDCOT_DATETIME","PDCOT_NONE","PDCOT_NUMBER","PDCOT_SIZE","PDCOT_STRING","PROPDESC_CONDITION_TYPE","PROPDESC_CONDITION_TYPE enumeration [Windows Properties]","properties.PROPDESC_CONDITION_TYPE","propsys/PDCOT_BOOLEAN","propsys/PDCOT_DATETIME","propsys/PDCOT_NONE","propsys/PDCOT_NUMBER","propsys/PDCOT_SIZE","propsys/PDCOT_STRING","propsys/PROPDESC_CONDITION_TYPE","shell.PROPDESC_CONDITION_TYPE","shell_PROPDESC_CONDITION_TYPE"]
old-location: properties\PROPDESC_CONDITION_TYPE.htm
tech.root: properties
ms.assetid: 35ed3b49-8b36-4681-bad6-1669c0da94e0
ms.date: 12/05/2018
ms.keywords: PDCOT_BOOLEAN, PDCOT_DATETIME, PDCOT_NONE, PDCOT_NUMBER, PDCOT_SIZE, PDCOT_STRING, PROPDESC_CONDITION_TYPE, PROPDESC_CONDITION_TYPE enumeration [Windows Properties], properties.PROPDESC_CONDITION_TYPE, propsys/PDCOT_BOOLEAN, propsys/PDCOT_DATETIME, propsys/PDCOT_NONE, propsys/PDCOT_NUMBER, propsys/PDCOT_SIZE, propsys/PDCOT_STRING, propsys/PROPDESC_CONDITION_TYPE, shell.PROPDESC_CONDITION_TYPE, shell_PROPDESC_CONDITION_TYPE
req.header: propsys.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Propsys.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: PROPDESC_CONDITION_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PROPDESC_CONDITION_TYPE
 - propsys/PROPDESC_CONDITION_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Propsys.h
api_name:
 - PROPDESC_CONDITION_TYPE
---

# PROPDESC_CONDITION_TYPE enumeration


## -description

Describes the condition type to use when displaying the property in the query builder UI in Windows Vista, but not in Windows 7 and later.

## -enum-fields

### -field PDCOT_NONE:0

The default value; it means the condition type is unspecified.

### -field PDCOT_STRING:1

Use the string condition type.

### -field PDCOT_SIZE:2

Use the size condition type.

### -field PDCOT_DATETIME:3

Use the date/time condition type.

### -field PDCOT_BOOLEAN:4

Use the Boolean condition type.

### -field PDCOT_NUMBER:5

Use the number condition type.

## -remarks

The flags in PROPDESC_CONDITION_TYPE affected the query string display in the <b>Advanced Query Builder</b> user interface in Windows Vista. In Windows 7 and later, the flags in PROPDESC_CONDITION_TYPE are not used.

