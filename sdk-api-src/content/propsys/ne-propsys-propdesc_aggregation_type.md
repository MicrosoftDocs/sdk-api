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

# PROPDESC_AGGREGATION_TYPE enumeration


## -description


Describes how property values are displayed when multiple items are selected. For a particular property, PROPDESC_AGGREGATION_TYPE describes how the property should be displayed when multiple items that have a value for the property are selected, such as whether the values should be summed, or averaged, or just displayed with the default "Multiple Values" string.


## -enum-fields




### -field PDAT_DEFAULT

Display the string "Multiple Values".


### -field PDAT_FIRST

Display the first value in the selection.


### -field PDAT_SUM

Display the sum of the selected values. This flag is never returned for data types <b>VT_LPWSTR</b>, <b>VT_BOOL</b>, and <b>VT_FILETIME</b>.


### -field PDAT_AVERAGE

Display the numerical average of the selected values. This flag is never returned for data types <b>VT_LPWSTR</b>, <b>VT_BOOL</b>, and <b>VT_FILETIME</b>.


### -field PDAT_DATERANGE

Display the date range of the selected values. This flag is returned only for values of the <b>VT_FILETIME</b> data type.


### -field PDAT_UNION

Display a concatenated string of all the values. The order of individual values in the string is undefined. The concatenated string omits duplicate values; if a value occurs more than once, it appears only once in the concatenated string.


### -field PDAT_MAX

Display the highest of the selected values.


### -field PDAT_MIN

Display the lowest of the selected values.


## -remarks



These values are defined in propsys.h and propsys.idl.



