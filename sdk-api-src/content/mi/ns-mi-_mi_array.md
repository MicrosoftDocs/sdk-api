---
UID: NS:mi._MI_Array
title: "_MI_Array"
author: windows-driver-content
description: Generalized type that represents an array. It can be generalized because all arrays are the same size, except the data element type will be specialized.
old-location: wmi_v2\mi_array.htm
old-project: wmi_v2
ms.assetid: c44e9a00-e0ec-48d3-9997-b998a31080b7
ms.author: windowsdriverdev
ms.date: 4/18/2018
ms.keywords: MI_Array, MI_Array structure [Windows Management Infrastructure (MI)], _MI_Array, mi/MI_Array, wmi._mi_array, wmi_v2.mi_array
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
req.typenames: MI_Array
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Mi.h
api_name:
-	MI_Array
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _MI_Array structure


## -description


Generalized type that represents an array.  It can be generalized because all arrays are the same size, except the data element type will be specialized.


## -struct-fields




### -field data

A pointer to the array of values.


### -field size

The number of elements in the array.

