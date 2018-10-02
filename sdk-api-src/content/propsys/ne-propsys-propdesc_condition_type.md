---
UID: NE:propsys.PROPDESC_CONDITION_TYPE
title: PROPDESC_CONDITION_TYPE
author: windows-sdk-content
description: Describes the condition type to use when displaying the property in the query builder UI in Windows Vista, but not in Windows 7 and later.
old-location: properties\PROPDESC_CONDITION_TYPE.htm
tech.root: properties
ms.assetid: 35ed3b49-8b36-4681-bad6-1669c0da94e0
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: PDCOT_BOOLEAN, PDCOT_DATETIME, PDCOT_NONE, PDCOT_NUMBER, PDCOT_SIZE, PDCOT_STRING, PROPDESC_CONDITION_TYPE, PROPDESC_CONDITION_TYPE enumeration [Windows Properties], properties.PROPDESC_CONDITION_TYPE, propsys/PDCOT_BOOLEAN, propsys/PDCOT_DATETIME, propsys/PDCOT_NONE, propsys/PDCOT_NUMBER, propsys/PDCOT_SIZE, propsys/PDCOT_STRING, propsys/PROPDESC_CONDITION_TYPE, shell.PROPDESC_CONDITION_TYPE, shell_PROPDESC_CONDITION_TYPE
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Propsys.h
api_name:
 - PROPDESC_CONDITION_TYPE
product: Windows
targetos: Windows
req.typenames: PROPDESC_CONDITION_TYPE
req.redist: 
---

# PROPDESC_CONDITION_TYPE enumeration


## -description


Describes the condition type to use when displaying the property in the query builder UI in Windows Vista, but not in Windows 7 and later.


## -enum-fields




### -field PDCOT_NONE

The default value; it means the condition type is unspecified.


### -field PDCOT_STRING

Use the string condition type.


### -field PDCOT_SIZE

Use the size condition type.


### -field PDCOT_DATETIME

Use the date/time condition type.


### -field PDCOT_BOOLEAN

Use the Boolean condition type.


### -field PDCOT_NUMBER

Use the number condition type.


## -remarks



The flags in PROPDESC_CONDITION_TYPE affected the query string display in the <b>Advanced Query Builder</b> user interface in Windows Vista. In Windows 7 and later, the flags in PROPDESC_CONDITION_TYPE are not used.



