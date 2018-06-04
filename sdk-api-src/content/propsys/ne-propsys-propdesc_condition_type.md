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



