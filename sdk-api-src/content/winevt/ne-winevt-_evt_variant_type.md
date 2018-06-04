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

# _EVT_VARIANT_TYPE enumeration


## -description


Defines the possible data types of a variant data item.


## -enum-fields




### -field EvtVarTypeNull

Null content that implies that the element that contains the content does not exist.


### -field EvtVarTypeString

A null-terminated Unicode string.


### -field EvtVarTypeAnsiString

A null-terminated ANSI string.


### -field EvtVarTypeSByte

A signed 8-bit integer value.


### -field EvtVarTypeByte

An unsigned 8-bit integer value.


### -field EvtVarTypeInt16

An signed 16-bit integer value.


### -field EvtVarTypeUInt16

An unsigned 16-bit integer value.


### -field EvtVarTypeInt32

A signed 32-bit integer value.


### -field EvtVarTypeUInt32

An unsigned 32-bit integer value.


### -field EvtVarTypeInt64

A signed 64-bit integer value.


### -field EvtVarTypeUInt64

An unsigned 64-bit integer value.


### -field EvtVarTypeSingle

A single-precision real value.


### -field EvtVarTypeDouble

A double-precision real value.


### -field EvtVarTypeBoolean

A Boolean value.


### -field EvtVarTypeBinary

A hexadecimal binary value.


### -field EvtVarTypeGuid

A GUID value.


### -field EvtVarTypeSizeT

An unsigned 32-bit or 64-bit integer value that contains a pointer address.


### -field EvtVarTypeFileTime

A FILETIME value.


### -field EvtVarTypeSysTime

 A SYSTEMTIME value.


### -field EvtVarTypeSid

A security identifier (<a href="https://msdn.microsoft.com/library/windows/hardware/ff556740">SID</a>) structure


### -field EvtVarTypeHexInt32

A 32-bit hexadecimal number.


### -field EvtVarTypeHexInt64

A 64-bit hexadecimal number.


### -field EvtVarTypeEvtHandle

An EVT_HANDLE value.


### -field EvtVarTypeEvtXml

A null-terminated Unicode string that contains XML.


## -see-also




<a href="https://msdn.microsoft.com/4b0f338b-0b66-4ba5-9e29-b15afe15a2d3">EVT_VARIANT</a>
 

 

