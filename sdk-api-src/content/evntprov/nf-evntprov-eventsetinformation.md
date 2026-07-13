---
UID: NF:evntprov.EventSetInformation
title: EventSetInformation function (evntprov.h)
description: Configures an ETW event provider.
helpviewer_keywords:
  [
    "EventSetInformation",
    "EventSetInformation function [ETW]",
    "etw.eventsetinformation",
    "evntprov/EventSetInformation",
  ]
old-location: etw\eventsetinformation.htm
tech.root: ETW
ms.assetid: e8b408ba-4bb5-4166-bf43-d18e4fe8de32
ms.date: 12/05/2018
ms.keywords:
  EventSetInformation, EventSetInformation function [ETW],
  etw.eventsetinformation, evntprov/EventSetInformation
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
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql:
targetos: Windows
req.typenames:
req.redist:
ms.custom: 19H1
f1_keywords:
  - EventSetInformation
  - evntprov/EventSetInformation
dev_langs:
  - c++
topic_type:
  - APIRef
  - kbSyntax
api_type:
  - DllExport
api_location:
  - Advapi32.dll
  - API-MS-Win-eventing-provider-l1-1-0.dll
  - KernelBase.dll
  - API-MS-Win-Eventing-Provider-L1-1-1.dll
api_name:
  - EventSetInformation
  - EtwSetInformation
---

# EventSetInformation function

## -description

Configures an ETW event provider.

## -parameters

### -param RegHandle [in]

Event provider registration handle. This is a handle returned by
[EventRegister](/windows/desktop/api/evntprov/nf-evntprov-eventregister).

### -param InformationClass [in]

[EVENT_INFO_CLASS](/windows/desktop/api/evntprov/ne-evntprov-event_info_class)
value that specifies the configuration operation to be performed on the event
provider.

### -param EventInformation [in]

Pointer to a buffer that contains data to be used when configuring the event
provider. The format of the data in this buffer depends on the value specified
in the _InformationClass_ parameter.

This value may be `NULL` if _InformationLength_ is zero.

### -param InformationLength [in]

The size (in bytes) of the data in the _EventInformation_ buffer.

## -returns

If the function succeeds, the return value is **ERROR_SUCCESS**.

If the function fails, the return value is one of the following error codes.

- **ERROR_INVALID_PARAMETER**: The parameter is incorrect. For example, this
  error is returned if the _RegHandle_ parameter is not a valid provider
  registration handle, if _EventInformation_ is **NULL** but _InformationLength_
  is nonzero, or if the specified _InformationLength_ is not valid for the given
  _InformationClass_.
- **ERROR_NOT_SUPPORTED**: The request is not supported. This error is returned
  if the _InformationClass_ parameter is not a recognized value.
- **Other**: Use
  [FormatMessage](/windows/desktop/api/winbase/nf-winbase-formatmessage) to
  obtain the message string for the returned error.

## -see-also

[EVENT_INFO_CLASS](/windows/desktop/api/evntprov/ne-evntprov-event_info_class)

[EventRegister](/windows/desktop/api/evntprov/nf-evntprov-eventregister)
