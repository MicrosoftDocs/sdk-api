---
UID: NS:winevt._EVT_VARIANT
title: "_EVT_VARIANT"
author: windows-driver-content
description: Contains event data or property values.
old-location: wes\evt_variant.htm
old-project: WES
ms.assetid: 4b0f338b-0b66-4ba5-9e29-b15afe15a2d3
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: "*PEVT_VARIANT, EVT_VARIANT, EVT_VARIANT structure [EventLog], PEVT_VARIANT, PEVT_VARIANT structure pointer [EventLog], _EVT_VARIANT, wes.evt_variant, winevt/PEVT_VARIANT, winevt/_EVT_VARIANT"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
req.typenames: EVT_VARIANT, *PEVT_VARIANT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	WinEvt.h
api_name:
-	EVT_VARIANT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _EVT_VARIANT structure


## -description


Contains  event data or property values.


## -struct-fields




### -field Count

The number of elements in the array of values. Use <b>Count</b> if the <b>Type</b> member has the <b>EVT_VARIANT_TYPE_ARRAY</b> flag set.


### -field Type

A flag that specifies the data type of the variant. For possible values, see the <a href="https://msdn.microsoft.com/13cf5e71-07bb-45ac-89f9-b76a26539dcd">EVT_VARIANT_TYPE</a> enumeration.

The variant contains an array of values, if the <b>EVT_VARIANT_TYPE_ARRAY</b> flag is set. The members that end in "Arr" contain arrays of values. For example, you would use the <b>StringArr</b> member to access the variant data if the type is EvtVarTypeString and the <b>EVT_VARIANT_TYPE_ARRAY</b> flag is set.

You can use the <a href="https://msdn.microsoft.com/d3a4a136-ca33-4dad-95ad-af1be6687843">EVT_VARIANT_TYPE_MASK</a> constant to mask out the array bit to determine the variant's type.


#### - AnsiStringArr

A pointer to an array of null-terminated ANSI strings.


#### - AnsiStringVal

A null-terminated ANSI string value.


#### - BinaryVal

A pointer to a hexadecimal binary value.


#### - BooleanArr

A pointer to an array of Boolean values.


#### - BooleanVal

A Boolean value.


#### - ByteArr

A pointer to an array of unsigned 8-bit values.


#### - ByteVal

An unsigned 8-bit integer value.


#### - DoubleArr

A pointer to an array of double precision real values.


#### - DoubleVal

A double precision real value.


#### - EvtHandleVal

An  EVT_HANDLE value.


#### - FileTimeArr

A pointer to an array of FILETIME values.


#### - FileTimeVal

An 8-byte FILETIME value.


#### - GuidArr

A pointer to an array of GUID values.


#### - GuidVal

A 16-byte GUID value.


#### - Int16Arr

A  pointer to an array of signed 16-bit values.


#### - Int16Val

A signed 16-bit integer value.


#### - Int32Arr

A pointer to an array of signed 32-bit values.


#### - Int32Val

A signed 32-bit integer value.


#### - Int64Arr

A pointer to an array of signed 64-bit values.


#### - Int64Val

A signed 64-bit integer value.


#### - SByteArr

A pointer to an array of signed 8-bit values.


#### - SByteVal

A signed 8-bit integer value.


#### - SidArr

A pointer to an array of  4-byte ASCII values.


#### - SidVal

A 4-byte ASCII value. A security identifier (<a href="https://msdn.microsoft.com/library/windows/hardware/ff556740">SID</a>) structure that uniquely identifies a user or group.


#### - SingleArr

A pointer to an array of single precision real values.


#### - SingleVal

A single precision real value.


#### - SizeTArr

A pointer to an array of size_t values.


#### - SizeTVal

A pointer address. The size of the address (4 bytes or 8 bytes) depends on whether the provider ran on a 32-bit or 64-bit operating system.


#### - StringArr

A pointer to an array of null-terminated Unicode strings.


#### - StringVal

A null-terminated Unicode string.


#### - SysTimeArr

A pointer to an array of SYSTEMTIME values.


#### - SysTimeVal

A SYSTEMTIME value.


#### - UInt16Arr

A pointer to an array of unsigned 16-bit values.


#### - UInt16Val

An unsigned 16-bit integer value.


#### - UInt32Arr

A pointer to an array of unsigned 32-bit values.


#### - UInt32Val

An unsigned 32-bit integer value.


#### - UInt64Arr

A pointer to an array of unsigned 64-bit values.


#### - UInt64Val

An unsigned 64-bit integer value.


#### - XmlVal

An XML string value.


#### - XmlValArr

A pointer to an array of XML string values.


## -see-also




<a href="https://msdn.microsoft.com/a77cfbac-9abd-41e1-8ce6-ba92de97eb64">EVT_SYSTEM_PROPERTY_ID</a>



<a href="https://msdn.microsoft.com/13cf5e71-07bb-45ac-89f9-b76a26539dcd">EVT_VARIANT_TYPE</a>



<a href="https://msdn.microsoft.com/d3a4a136-ca33-4dad-95ad-af1be6687843">EVT_VARIANT_TYPE_MASK</a>
 

 

