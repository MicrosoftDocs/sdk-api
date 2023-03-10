---
UID: NS:mi._MI_Array
title: MI_Array (mi.h)
description: Generalized type that represents an array. It can be generalized because all arrays are the same size, except the data element type will be specialized.
helpviewer_keywords: ["MI_Array","MI_Array structure [Windows Management Infrastructure (MI)]","mi/MI_Array","wmi._mi_array","wmi_v2.mi_array"]
old-location: wmi_v2\mi_array.htm
tech.root: wmi_v2
ms.assetid: c44e9a00-e0ec-48d3-9997-b998a31080b7
ms.date: 12/05/2018
ms.keywords: MI_Array, MI_Array structure [Windows Management Infrastructure (MI)], mi/MI_Array, wmi._mi_array, wmi_v2.mi_array
req.header: mi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
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
req.typenames: MI_Array
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
ms.custom: 19H1
f1_keywords:
 - _MI_Array
 - mi/_MI_Array
 - MI_Array
 - mi/MI_Array
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mi.h
api_name:
 - MI_Array
---

# MI_Array structure


## -description

Generalized type that represents an array.  It can be generalized because all arrays are the same size, except the data element type will be specialized.

## -struct-fields

### -field data

A pointer to the array of values.

### -field size

The number of elements in the array.

