---
UID: NS:evntprov._EVENT_DATA_DESCRIPTOR
title: EVENT_DATA_DESCRIPTOR (evntprov.h)
description:
  The EVENT_DATA_DESCRIPTOR structure defines a block of data that will be used
  in an ETW event.
helpviewer_keywords:
  [
    "*PEVENT_DATA_DESCRIPTOR",
    "EVENT_DATA_DESCRIPTOR",
    "EVENT_DATA_DESCRIPTOR structure [ETW]",
    "PEVENT_DATA_DESCRIPTOR",
    "PEVENT_DATA_DESCRIPTOR structure pointer [ETW]",
    "_EVENT_DATA_DESCRIPTOR",
    "base.event_data_descriptor",
    "etw.event_data_descriptor",
    "evntprov/EVENT_DATA_DESCRIPTOR",
    "evntprov/PEVENT_DATA_DESCRIPTOR",
  ]
old-location: etw\event_data_descriptor.htm
tech.root: ETW
ms.assetid: 452ce6f6-3857-4f88-b501-44dd6091b97e
ms.date: 12/05/2018
ms.keywords:
  "*PEVENT_DATA_DESCRIPTOR, EVENT_DATA_DESCRIPTOR, EVENT_DATA_DESCRIPTOR
  structure [ETW], PEVENT_DATA_DESCRIPTOR, PEVENT_DATA_DESCRIPTOR structure
  pointer [ETW], _EVENT_DATA_DESCRIPTOR, base.event_data_descriptor,
  etw.event_data_descriptor, evntprov/EVENT_DATA_DESCRIPTOR,
  evntprov/PEVENT_DATA_DESCRIPTOR"
req.header: evntprov.h
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
targetos: Windows
req.typenames: EVENT_DATA_DESCRIPTOR, *PEVENT_DATA_DESCRIPTOR
req.redist:
ms.custom: 19H1
f1_keywords:
  - _EVENT_DATA_DESCRIPTOR
  - evntprov/_EVENT_DATA_DESCRIPTOR
  - PEVENT_DATA_DESCRIPTOR
  - evntprov/PEVENT_DATA_DESCRIPTOR
  - EVENT_DATA_DESCRIPTOR
  - evntprov/EVENT_DATA_DESCRIPTOR
dev_langs:
  - c++
topic_type:
  - APIRef
  - kbSyntax
api_type:
  - HeaderDef
api_location:
  - Evntprov.h
api_name:
  - EVENT_DATA_DESCRIPTOR
---

# EVENT_DATA_DESCRIPTOR structure

## -description

The **EVENT_DATA_DESCRIPTOR** structure defines a block of data that will be
used in an ETW event.

This structure is typically initialized using the
[EventDataDescCreate](/windows/win32/api/evntprov/nf-evntprov-eventdatadesccreate)
function.

## -struct-fields

### -field Ptr

A pointer to the data.

> [!Important]
> This is a 64-bit unsigned integer value in both 32-bit and
> 64-bit architectures. To properly set this value, cast your data pointer to an
> unsigned integer before assigning it to the `Ptr` field, e.g.
> `EventDataDescriptor.Ptr = (UINT_PTR)dataPointer;`, or use the
> [EventDataDescCreate](/windows/win32/api/evntprov/nf-evntprov-eventdatadesccreate)
> function.

### -field Size

The size of the data in bytes.

### -field DUMMYUNIONNAME

### -field DUMMYUNIONNAME.Reserved

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.Type

Specifies the use of this data in the event. This can be one of the following
values:

- **EVENT_DATA_DESCRIPTOR_TYPE_NONE** (0)

  Normal event data.

- **EVENT_DATA_DESCRIPTOR_TYPE_EVENT_METADATA** (1)

  TraceLogging event decoding information.

- **EVENT_DATA_DESCRIPTOR_TYPE_PROVIDER_METADATA** (2)

  Manually-attached provider traits. For use with operating systems that do not
  support attaching provider traits via EventSetInformation. This data will be
  ignored if provider traits have been configured via `EventSetInformation`.

- **EVENT_DATA_DESCRIPTOR_TYPE_TIMESTAMP_OVERRIDE** (3)

  64-bit event timestamp override. For use when relogging. Note that logging
  events out of timestamp order may lead to event ordering issues during trace
  processing.

Note that this field will be ignored unless the event provider has been
configured to respect the `Type` field by calling the
[EventSetInformation](/windows/win32/api/evntprov/nf-evntprov-eventsetinformation)
API with the `EventProviderSetTraits` or `EventProviderUseDescriptorType`
operation.

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.Reserved1

Not used. Set to 0.

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.Reserved2

Not used. Set to 0.

## -remarks

Most event providers will not call **EventDataDescCreate** directly. Instead,
most event providers are implemented using an ETW framework that wraps the calls
to **EventRegister**, **EventWrite**, and **EventUnregister**. For example, you
might
[write an event manifest](/windows/win32/etw/writing-manifest-based-events) and
then use the [Message Compiler](/windows/win32/wes/message-compiler--mc-exe-) to
generate C/C++ code for the events, or you might use
[TraceLogging](/windows/win32/tracelogging/trace-logging-portal) to avoid the
need for a manifest.

To write an event that contains event data, you would create an array of
**EVENT_DATA_DESCRIPTOR** structures (one element for each chunk of data) and
call the
[EventDataDescCreate](/windows/desktop/api/evntprov/nf-evntprov-eventdatadesccreate)
function to initialize each element with the data to be included in your event.
You would then pass this array to
[EventWrite](/windows/desktop/api/evntprov/nf-evntprov-eventwrite) to include
the data into the event. For an example, see
[Writing Manifest-based Events](/windows/desktop/ETW/writing-manifest-based-events).

The data written to the event will be the concatenation of the data chunks
referenced by the **EVENT_DATA_DESCRIPTOR** structures passed to the
`EventWrite` function. This concatenation contains no padding and does not
retain any of the boundaries or size information from the original set of data
chunks.

The total size of an ETW event (the sum of the user-provided data, the
[EVENT_HEADER](/windows/desktop/api/evntcons/ns-evntcons-event_header), and any
[EVENT_HEADER_EXTENDED_DATA_ITEM](/windows/desktop/api/evntcons/ns-evntcons-event_header_extended_data_item)
that might be needed for the event) cannot exceed 64KB. Events larger than 64KB
will be dropped by the ETW runtime.

In addition, ETW events that cannot fit into a trace session buffer will also be
dropped. Each buffer has a 72-byte header, so the largest event that can fit
into a buffer is slightly smaller than the buffer's size. For example, a trace
session that uses 32KB buffers will not be able to accept any event larger than
32,696 bytes (32,768-byte buffer minus the 72-byte header leaves 32,696 bytes
for events).

## -see-also

[EVENT_HEADER](/windows/desktop/api/evntcons/ns-evntcons-event_header)

[EVENT_HEADER_EXTENDED_DATA_ITEM](/windows/desktop/api/evntcons/ns-evntcons-event_header_extended_data_item)

[EventDataDescCreate](/windows/win32/api/evntprov/nf-evntprov-eventdatadesccreate)

[EventWrite](/windows/desktop/api/evntprov/nf-evntprov-eventwrite)

[EventWriteTransfer](/windows/desktop/api/evntprov/nf-evntprov-eventwritetransfer)

[Writing Manifest-based Events](/windows/desktop/ETW/writing-manifest-based-events)
