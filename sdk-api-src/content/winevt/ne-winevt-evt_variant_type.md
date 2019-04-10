---
UID: NE:winevt._EVT_VARIANT_TYPE
title: EVT_VARIANT_TYPE (winevt.h)
author: windows-sdk-content
description: Defines the possible data types of a variant data item.
old-location: wes\evt_variant_type.htm
tech.root: wes
ms.assetid: 13cf5e71-07bb-45ac-89f9-b76a26539dcd
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: EVT_VARIANT_TYPE, EvtVarTypeAnsiString, EvtVarTypeBinary, EvtVarTypeBoolean, EvtVarTypeByte, EvtVarTypeDouble, EvtVarTypeEvtHandle, EvtVarTypeEvtXml, EvtVarTypeFileTime, EvtVarTypeGuid, EvtVarTypeHexInt32, EvtVarTypeHexInt64, EvtVarTypeInt16, EvtVarTypeInt32, EvtVarTypeInt64, EvtVarTypeNull, EvtVarTypeSByte, EvtVarTypeSid, EvtVarTypeSingle, EvtVarTypeSizeT, EvtVarTypeString, EvtVarTypeSysTime, EvtVarTypeUInt16, EvtVarTypeUInt32, EvtVarTypeUInt64, _EVT_VARIANT_TYPE, _EVT_VARIANT_TYPE enumeration [EventLog], wes.evt_variant_type, winevt/EvtVarTypeAnsiString, winevt/EvtVarTypeBinary, winevt/EvtVarTypeBoolean, winevt/EvtVarTypeByte, winevt/EvtVarTypeDouble, winevt/EvtVarTypeEvtHandle, winevt/EvtVarTypeEvtXml, winevt/EvtVarTypeFileTime, winevt/EvtVarTypeGuid, winevt/EvtVarTypeHexInt32, winevt/EvtVarTypeHexInt64, winevt/EvtVarTypeInt16, winevt/EvtVarTypeInt32, winevt/EvtVarTypeInt64, winevt/EvtVarTypeNull, winevt/EvtVarTypeSByte, winevt/EvtVarTypeSid, winevt/EvtVarTypeSingle, winevt/EvtVarTypeSizeT, winevt/EvtVarTypeString, winevt/EvtVarTypeSysTime, winevt/EvtVarTypeUInt16, winevt/EvtVarTypeUInt32, winevt/EvtVarTypeUInt64, winevt/_EVT_VARIANT_TYPE
ms.topic: enum
req.header: winevt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinEvt.h
api_name:
 - EVT_VARIANT_TYPE
product: Windows
targetos: Windows
req.typenames: EVT_VARIANT_TYPE
req.redist: 
---

# EVT_VARIANT_TYPE enumeration


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

A security identifier (<a href="https://msdn.microsoft.com/328fba4e-e590-4174-9274-52dad58cb91f">SID</a>) structure


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
 

 

