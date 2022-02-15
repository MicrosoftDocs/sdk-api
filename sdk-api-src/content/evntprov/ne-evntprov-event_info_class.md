---
UID: NE:evntprov._EVENT_INFO_CLASS
title: EVENT_INFO_CLASS (evntprov.h)
description:
  The EVENT_INFO_CLASS enumeration type is used with the EventSetInformation
  function to specify the configuration operation to be performed on an ETW
  event provider registration.
helpviewer_keywords:
  [
    "EVENT_INFO_CLASS",
    "EVENT_INFO_CLASS enumeration [ETW]",
    "EventProviderBinaryTrackInfo",
    "EventProviderSetTraits",
    "EventProviderUseDescriptorType",
    "MaxEventInfo",
    "etw.event_info_class",
    "evntprov/EVENT_INFO_CLASS",
    "evntprov/EventProviderBinaryTrackInfo",
    "evntprov/EventProviderSetTraits",
    "evntprov/EventProviderUseDescriptorType",
    "evntprov/MaxEventInfo",
  ]
old-location: etw\event_info_class.htm
tech.root: ETW
ms.assetid: 76ac2b93-d5df-4504-b36d-1530bbb12ab4
ms.date: 12/05/2018
ms.keywords:
  EVENT_INFO_CLASS, EVENT_INFO_CLASS enumeration [ETW],
  EventProviderBinaryTrackInfo, EventProviderSetTraits,
  EventProviderUseDescriptorType, MaxEventInfo, etw.event_info_class,
  evntprov/EVENT_INFO_CLASS, evntprov/EventProviderBinaryTrackInfo,
  evntprov/EventProviderSetTraits, evntprov/EventProviderUseDescriptorType,
  evntprov/MaxEventInfo
req.header: evntprov.h
req.include-header:
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
req.typenames: EVENT_INFO_CLASS
req.redist:
ms.custom: 19H1
f1_keywords:
  - _EVENT_INFO_CLASS
  - evntprov/_EVENT_INFO_CLASS
  - EVENT_INFO_CLASS
  - evntprov/EVENT_INFO_CLASS
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
  - EVENT_INFO_CLASS
---

# EVENT_INFO_CLASS enumeration

## -description

The **EVENT_INFO_CLASS** enumeration type is used with the
[EventSetInformation](/windows/desktop/api/evntprov/nf-evntprov-eventsetinformation)
function to specify the configuration operation to be performed on an ETW event
provider registration.

## -enum-fields

### -field EventProviderBinaryTrackInfo

Adds binary tracking information from this provider to each session that
collects events from this event provider. The binary tracking data includes the
full path to the binary containing the callback that was specified when
registering the event provider. This information is useful if the binary
contains [mc.exe](/windows/win32/wes/message-compiler--mc-exe-)-generated
decoding resources but is not globally registered. Decoding tools can use the
path in the trace to locate the binary and extract the decoding resources.

The _EventInformation_ buffer is not used with this configuration operation. The
ETW runtime will automatically use the full path of the caller's module (the
full path to the DLL or EXE that contains the callback function specified in the
call to **EventRegister**). For this operation to be useful, the same DLL or EXE
file must contain the `mc.exe`-generated decoding resources.

### -field EventProviderSetReserved1

Not used.

### -field EventProviderSetTraits

Sets traits for the provider such as the provider's name. Indicates that ETW
should recognize the `Type` field of
[EVENT_DATA_DESCRIPTOR](ns-evntprov-event_data_descriptor.md) structures used
with this provider. Requires the provider to initialize all fields of the
**EVENT_DATA_DESCRIPTOR** structures, including the `Reserved` field. (The
provider should usually set `dataDescriptor.Reserved = 0`, as is done by
[EventDataDescCreate](nf-evntprov-eventdatadesccreate.md).)

Note that the **EVENT_DATA_DESCRIPTOR** structure contains a `Type` field in a
section of the structure that was previously the `Reserved` field. To avoid
compatibility issues with providers that leave the Reserved field uninitialized,
ETW will ignore the `Type` field (treat it as 0) unless the provider has used
_EventProviderSetTraits_ or _EventProviderUseDescriptorType_ in a call to
**EventSetInformation**.

The _EventInformation_ buffer should contain the
[provider traits](/windows/desktop/ETW/provider-traits) to be used for the
provider.

### -field EventProviderUseDescriptorType

Specifies whether ETW should recognize the `Type` field of
[EVENT_DATA_DESCRIPTOR](ns-evntprov-event_data_descriptor.md) structures used
with this provider. If `TRUE`, requires the provider to initialize all fields of
the **EVENT_DATA_DESCRIPTOR** structures, including the `Reserved` field. (The
provider should usually set `dataDescriptor.Reserved = 0`, as is done by
[EventDataDescCreate](nf-evntprov-eventdatadesccreate.md).)

Note that the **EVENT_DATA_DESCRIPTOR** structure contains a `Type` field in a
section of the structure that was previously the `Reserved` field. To avoid
compatibility issues with providers that leave the Reserved field uninitialized,
ETW will ignore the `Type` field (treat it as 0) unless the provider has used
_EventProviderSetTraits_ or _EventProviderUseDescriptorType_ in a call to
**EventSetInformation**.

The _EventInformation_ buffer should contain a **BOOLEAN** value (1 byte, value
`FALSE` or `TRUE`).

### -field MaxEventInfo

The first invalid operation code. This value may change in subsequent versions
of the Windows SDK.

## -see-also

[EventSetInformation](/windows/desktop/api/evntprov/nf-evntprov-eventsetinformation)

[Provider Traits](/windows/desktop/ETW/provider-traits)
