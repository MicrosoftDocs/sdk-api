---
UID: NF:tdh.TdhFormatProperty
title: TdhFormatProperty function (tdh.h)
description: Formats a property value for display.
helpviewer_keywords: ["TdhFormatProperty","TdhFormatProperty function [ETW]","etw.tdhformatproperty","tdh/TdhFormatProperty"]
old-location: etw\tdhformatproperty.htm
tech.root: ETW
ms.assetid: ecc954f8-840e-4963-a0c8-64aac25355e3
ms.date: 12/05/2018
ms.keywords: TdhFormatProperty, TdhFormatProperty function [ETW], etw.tdhformatproperty, tdh/TdhFormatProperty
req.header: tdh.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Tdh.lib
req.dll: Tdh.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - TdhFormatProperty
 - tdh/TdhFormatProperty
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-eventing-tdh-l1-1-2.dll
 - api-ms-win-eventing-tdh-l1-1-1.dll
 - Tdh.dll
 - API-MS-Win-Eventing-Tdh-L1-1-0.dll
 - MinTdh.dll
api_name:
 - TdhFormatProperty
---

# TdhFormatProperty function

## -description

Formats a property value for display.

## -parameters

### -param EventInfo [in]

A [TRACE_EVENT_INFO structure](ns-tdh-trace_event_info.md) that contains the event information. To get this structure, call the [TdhGetEventInformation function](nf-tdh-tdhgeteventinformation.md).

### -param MapInfo [in, optional]

An [EVENT_MAP_INFO structure](ns-tdh-event_map_info.md) that maps integer and bit values to strings. To get this structure, call the [TdhGetEventMapInformation function](nf-tdh-tdhgeteventmapinformation.md). To get the name of the map, use the **MapNameOffset** member of the [EVENT_PROPERTY_INFO structure](ns-tdh-event_property_info.md). If you do not provide the map information for a mapped property, the function formats the integer or bit value.

### -param PointerSize [in]

The size of a pointer value in the event data. To get the size, access the [EVENT_RECORD.EventHeader.Flags](../evntcons/ns-evntcons-event_header.md) member. The pointer size is 4 bytes if the EVENT_HEADER_FLAG_32_BIT_HEADER flag is set; otherwise, it is 8 bytes if the EVENT_HEADER_FLAG_64_BIT_HEADER flag is set. The [EVENT_RECORD structure (evntcons.h)](../evntcons/ns-evntcons-event_record.md) is passed to your [PEVENT_RECORD_CALLBACK callback function].

### -param PropertyInType [in]

The input type of the property. Use the **InType** member of the [EVENT_PROPERTY_INFO structure](ns-tdh-event_property_info.md) to set this parameter.

### -param PropertyOutType [in]

The output type of the property. Use the **OutType** member of the [EVENT_PROPERTY_INFO structure](ns-tdh-event_property_info.md) to set this parameter.

### -param PropertyLength [in]

The length, in bytes, of the property. Use the **Length** member of the [EVENT_PROPERTY_INFO structure](ns-tdh-event_property_info.md) to set this parameter.

### -param UserDataLength [in]

The size, in bytes, of the *UserData* buffer. See Remarks.

### -param UserData [in]

The buffer that contains the event data. See Remarks.

### -param BufferSize [in, out]

The size, in bytes, of the *Buffer* buffer. If the function succeeds, this parameter receives the size of the buffer used. If the buffer is too small, the function returns ERROR_INSUFFICIENT_BUFFER and sets this parameter to the required buffer size. If the buffer size is zero on input, no data is returned in the buffer and this parameter receives the required buffer size.

### -param Buffer [out, optional]

A caller-allocated buffer that contains the formatted property value. To determine the required buffer size, set this parameterto **NULL** and *BufferSize* to zero.

### -param UserDataConsumed [out]

The length, in bytes, of the consumed event data. Use this value to adjust the values of the *UserData* and *UserDataLength* parameters. See Remarks.

## -returns

Returns ERROR_SUCCESS if successful. Otherwise, this function returns one of the following return codes in addition to others.

| Return code | Description |
| -- | -- |
| **ERROR_INSUFFICIENT_BUFFER** | The size of the *pBuffer* buffer is too small. Use the required buffer size set in *pBufferSize* to allocate a new buffer. |
| **ERROR_INVALID_PARAMETER** | One or more of the parameters is not valid. |
| **ERROR_EVT_INVALID_EVENT_DATA** | The event data does not match the event definition in the manifest. |

## -remarks

Typically, you call this function in a loop. Use the [TRACE_EVENT_INFO.TopLevelPropertyCount](ns-tdh-trace_event_info.md) member to control the loop (the [TdhGetEventInformation function](nf-tdh-tdhgeteventinformation.md) returns the [TRACE_EVENT_INFO structure](ns-tdh-trace_event_info.md)). Before entering the loop, you set the *UserData* and *UserDataLength* parameters to the value of the **UserData** and **UserDataLength** members of the [EVENT_RECORD structure](../evntcons/ns-evntcons-event_record.md), respectively. The [EVENT_RECORD structure](../evntcons/ns-evntcons-event_record.md) is passed to your [PEVENT_RECORD_CALLBACK callback function].

Determine whether the property is an array. The property is an array if the [EVENT_PROPERTY_INFO.Flags](ns-tdh-event_property_info.md) member is set to PropertyParamCount or the [EVENT_PROPERTY_INFO.count](ns-tdh-event_property_info.md) member is greater than 1. Call the **TdhFormatProperty** function in a loop based on the number of elements in the array.

After calling the **TdhFormatProperty** function, use the *UserDataConsumed* parameter value to set the new values of the *UserData* and *UserDataLength* parameters (Subtract *UserDataConsumed* from *UserDataLength* and use *UserDataLength* to increment the *UserData* pointer).

If the property is an IP V6 address, you must set the *PropertyLength* parameter to the size of the **IN6_ADDR** structure. The property is considered an IP V6 address if the following conditions are met:

- The **InType** member of the [EVENT_PROPERTY_INFO structure](ns-tdh-event_property_info.md) is TDH_INTYPE_BINARY
- The **OutType** member of the [EVENT_PROPERTY_INFO structure](ns-tdh-event_property_info.md) is TDH_OUTTYPE_IPV6
- The **Length** member of the [EVENT_PROPERTY_INFO structure](ns-tdh-event_property_info.md) is 0

### Examples

For an example that shows how to call this function , see [Using TdhFormatProperty to Consume Event Data](/windows/win32/etw/using-tdhformatproperty-to-consume-event-data).
