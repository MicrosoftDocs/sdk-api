---
UID: NE:propsys.PROPDESC_AGGREGATION_TYPE
title: PROPDESC_AGGREGATION_TYPE (propsys.h)
description: Describes how property values are displayed when multiple items are selected.
helpviewer_keywords: ["PDAT_AVERAGE","PDAT_DATERANGE","PDAT_DEFAULT","PDAT_FIRST","PDAT_MAX","PDAT_MIN","PDAT_SUM","PDAT_UNION","PROPDESC_AGGREGATION_TYPE","PROPDESC_AGGREGATION_TYPE enumeration [Windows Properties]","_shell_PROPDESC_AGGREGATION_TYPE","properties.PROPDESC_AGGREGATION_TYPE","propsys/PDAT_AVERAGE","propsys/PDAT_DATERANGE","propsys/PDAT_DEFAULT","propsys/PDAT_FIRST","propsys/PDAT_MAX","propsys/PDAT_MIN","propsys/PDAT_SUM","propsys/PDAT_UNION","propsys/PROPDESC_AGGREGATION_TYPE","shell.PROPDESC_AGGREGATION_TYPE"]
old-location: properties\PROPDESC_AGGREGATION_TYPE.htm
tech.root: properties
ms.assetid: 7f42d7dd-cc8e-444f-a4df-2d67362486f2
ms.date: 12/05/2018
ms.keywords: PDAT_AVERAGE, PDAT_DATERANGE, PDAT_DEFAULT, PDAT_FIRST, PDAT_MAX, PDAT_MIN, PDAT_SUM, PDAT_UNION, PROPDESC_AGGREGATION_TYPE, PROPDESC_AGGREGATION_TYPE enumeration [Windows Properties], _shell_PROPDESC_AGGREGATION_TYPE, properties.PROPDESC_AGGREGATION_TYPE, propsys/PDAT_AVERAGE, propsys/PDAT_DATERANGE, propsys/PDAT_DEFAULT, propsys/PDAT_FIRST, propsys/PDAT_MAX, propsys/PDAT_MIN, propsys/PDAT_SUM, propsys/PDAT_UNION, propsys/PROPDESC_AGGREGATION_TYPE, shell.PROPDESC_AGGREGATION_TYPE
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
req.typenames: PROPDESC_AGGREGATION_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PROPDESC_AGGREGATION_TYPE
 - propsys/PROPDESC_AGGREGATION_TYPE
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
 - PROPDESC_AGGREGATION_TYPE
---

# PROPDESC_AGGREGATION_TYPE enumeration


## -description

Describes how property values are displayed when multiple items are selected. For a particular property, PROPDESC_AGGREGATION_TYPE describes how the property should be displayed when multiple items that have a value for the property are selected, such as whether the values should be summed, or averaged, or just displayed with the default "Multiple Values" string.

## -enum-fields

### -field PDAT_DEFAULT:0

Display the string "Multiple Values".

### -field PDAT_FIRST:1

Display the first value in the selection.

### -field PDAT_SUM:2

Display the sum of the selected values. This flag is never returned for data types <b>VT_LPWSTR</b>, <b>VT_BOOL</b>, and <b>VT_FILETIME</b>.

### -field PDAT_AVERAGE:3

Display the numerical average of the selected values. This flag is never returned for data types <b>VT_LPWSTR</b>, <b>VT_BOOL</b>, and <b>VT_FILETIME</b>.

### -field PDAT_DATERANGE:4

Display the date range of the selected values. This flag is returned only for values of the <b>VT_FILETIME</b> data type.

### -field PDAT_UNION:5

Display a concatenated string of all the values. The order of individual values in the string is undefined. The concatenated string omits duplicate values; if a value occurs more than once, it appears only once in the concatenated string.

### -field PDAT_MAX:6

Display the highest of the selected values.

### -field PDAT_MIN:7

Display the lowest of the selected values.

## -remarks

These values are defined in propsys.h and propsys.idl.

