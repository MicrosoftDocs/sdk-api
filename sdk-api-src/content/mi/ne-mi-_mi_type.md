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

# _MI_Type enumeration


## -description


These
values specify the data type of qualifiers, properties, references,
parameters, and method return values for the CIM data types.


## -enum-fields




### -field MI_BOOLEAN

unsigned char


### -field MI_UINT8

unsigned char


### -field MI_SINT8

signed char


### -field MI_UINT16

unsigned short


### -field MI_SINT16

signed short


### -field MI_UINT32

unsigned int


### -field MI_SINT32

signed int


### -field MI_UINT64

unsigned __int64


### -field MI_SINT64

signed __int64


### -field MI_REAL32

float


### -field MI_REAL64

double


### -field MI_CHAR16

unsigned short


### -field MI_DATETIME

Structure holding a union of <a href="https://msdn.microsoft.com/f06f1b0e-d21c-4b60-8099-222a1582fde1">MI_Timestamp</a> or <a href="https://msdn.microsoft.com/b6bf3d47-c292-4140-8bc6-f15ad8a8019f">MI_Interval</a>.


### -field MI_STRING

MI_CHAR*


### -field MI_REFERENCE

This is encoded as an <a href="https://msdn.microsoft.com/3dce1817-7995-49e5-8cc0-ee9496665e5c">MI_Instance</a>, but usually only the key properties are set.


### -field MI_INSTANCE


### -field MI_BOOLEANA

Array of <b>MI_BOOLEAN</b> types.


### -field MI_UINT8A

Array of <b>MI_UINT8</b> types.


### -field MI_SINT8A

Array of <b>MI_SINT8</b> types.


### -field MI_UINT16A

Array of <b>MI_UINT16</b> types.


### -field MI_SINT16A

Array of <b>MI_SINT16</b> types.


### -field MI_UINT32A

Array of <b>MI_UINT32</b> types.


### -field MI_SINT32A

Array of <b>MI_SINT32</b> types.


### -field MI_UINT64A

Array of <b>MI_UINT64</b> types.


### -field MI_SINT64A

Array of <b>MI_SINT64</b> types.


### -field MI_REAL32A

Array of <b>MI_REAL32</b> types.


### -field MI_REAL64A

Array of <b>MI_REAL64</b> types.


### -field MI_CHAR16A

Array of <b>MI_CHAR16</b> types.


### -field MI_DATETIMEA

Array of <b>MI_DATETIME</b> structures.


### -field MI_STRINGA

Array of <b>MI_STRING</b> types.


### -field MI_REFERENCEA

Array of <b>MI_REFERENCE</b> types.


### -field MI_INSTANCEA

Array of <b>MI_INSTANCE</b> types.


### -field MI_ARRAY

MI_ARRAY is not an actual type, rather this is the bit that signifies  the type is an array.

