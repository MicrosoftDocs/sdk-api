---
UID: NS:nvme.NVME_CDW11_FEATURE_ASYNC_EVENT_CONFIG
tech.root: fs
title: NVME_CDW11_FEATURE_ASYNC_EVENT_CONFIG
ms.date: 02/19/2021
ms.topic: language-reference
targetos: Windows
description: Contains parameters for the Asynchronous Event Configuration Feature that controls the events that trigger an asynchronous event notification to the host.
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: nvme.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: Windows 10
req.target-min-winversvr: 
req.target-type: 
req.typenames: NVME_CDW11_FEATURE_ASYNC_EVENT_CONFIG, *PNVME_CDW11_FEATURE_ASYNC_EVENT_CONFIG
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - nvme.h
api_name:
 - PNVME_CDW11_FEATURE_ASYNC_EVENT_CONFIG
 - NVME_CDW11_FEATURE_ASYNC_EVENT_CONFIG
f1_keywords:
 - PNVME_CDW11_FEATURE_ASYNC_EVENT_CONFIG
 - nvme/PNVME_CDW11_FEATURE_ASYNC_EVENT_CONFIG
 - NVME_CDW11_FEATURE_ASYNC_EVENT_CONFIG
 - nvme/NVME_CDW11_FEATURE_ASYNC_EVENT_CONFIG
dev_langs:
 - c++
---

# NVME_CDW11_FEATURE_ASYNC_EVENT_CONFIG structure


## -description

Contains parameters for the Asynchronous Event Configuration Feature that controls the events that trigger an asynchronous event notification to the host.

The values from this structure are used in the **AsyncEventConfig** field of the [NVME_CDW11_FEATURES](ns-nvme-nvme_cdw11_features.md) structure.

## -struct-fields

### -field DUMMYSTRUCTNAME

### -field DUMMYSTRUCTNAME.CriticalWarnings

Specifies whether an asynchronous event notification is sent to the host for the corresponding Critical Warning specified in the **CriticalWarning** field of the [SMART / Health Information Log](ns-nvme-nvme_health_info_log.md).

When the value in this field is set to `1`, an asynchronous event notification is sent when the corresponding **CriticalWarning** field is set to `1` in the SMART / Health Information Log. When the value in this field is set to `0`, an asynchronous event notification is not sent when the corresponding **CriticalWarning** field is set to `1` in the SMART / Health Information Log.

### -field DUMMYSTRUCTNAME.NsAttributeNotices

Specifies whether an asynchronous event notification is sent to the host for a Namespace Attribute change [NVME_ASYNC_NOTICE_NAMESPACE_ATTRIBUTE_CHANGED](ne-nvme-nvme_async_event_notice_codes.md).

When the value in this field is set to `1`, the Namespace Attribute Changed event is sent to the host when this condition occurs. When the value in this field is cleared to `0`, the controller will not send the Namespace Attribute Changed event to the host.

### -field DUMMYSTRUCTNAME.FwActivationNotices

Specifies whether an asynchronous event notification is sent to the host for a Firmware Activation Starting event [NVME_ASYNC_NOTICE_FIRMWARE_ACTIVATION_STARTING](ne-nvme-nvme_async_event_notice_codes.md). 

When the value in this field is set to `1`, the Firmware Activation Starting event is sent to the host when this condition occurs. When the value in this field is cleared to `0`, the controller will not send the Firmware Activation Starting event to the host.

### -field DUMMYSTRUCTNAME.Reserved0

### -field DUMMYSTRUCTNAME.TelemetryLogNotices

Specifies whether an asynchronous event notification is sent to the host for a Telemetry Log Changed event [NVME_ASYNC_NOTICE_TELEMETRY_LOG_CHANGED](ne-nvme-nvme_async_event_notice_codes.md).

### -field AsUlong

## -remarks

The Asynchronous Event Configuration Feature can be used to disable reporting events in the case of a persistent condition.

## -see-also

- [NVME_ASYNC_EVENT_NOTICE_CODES](ne-nvme-nvme_async_event_notice_codes.md)
- [NVME_CDW11_FEATURES](ns-nvme-nvme_cdw11_features.md)

