---
UID: NE:audioengineextensionapo.APO_LOG_LEVEL
tech.root: audio
title: APO_LOG_LEVEL
ms.date: 06/19/2021
targetos: Windows
description: Specifies the level of an APO event logged with IAudioProcessingObjectLoggingService::ApoLog.
prerelease: false
req.construct-type: enumeration
req.ddi-compliance: 
req.header: audioengineextensionapo.h
req.include-header: 
req.kmdf-ver: 
req.max-support: 
req.target-min-winverclnt: Windows Build 22000
req.target-min-winversvr: 
req.target-type: 
req.typenames: 
req.umdf-ver: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - audioengineextensionapo.h
api_name:
 - APO_LOG_LEVEL
f1_keywords:
 - APO_LOG_LEVEL
 - audioengineextensionapo/APO_LOG_LEVEL
dev_langs:
 - c++
---

## -description

Specifies the level of an APO event logged with [IAudioProcessingObjectLoggingService::ApoLog](nf-audioengineextensionapo-iaudioprocessingobjectloggingservice-apolog.md).

## -enum-fields

### -field APO_LOG_LEVEL_ALWAYS:0

All events.

### -field APO_LOG_LEVEL_CRITICAL:1

Abnormal exit or termination events.

### -field APO_LOG_LEVEL_ERROR:2

Severe error events.

### -field APO_LOG_LEVEL_WARNING:3

Warning events such as allocation failures.

### -field APO_LOG_LEVEL_INFO:4

Non-error events such as entry or exit events.

### -field APO_LOG_LEVEL_VERBOSE:5

Detailed trace events.

## -remarks

For more information on the Windows 11 APIs for the Audio Processing Objects (APOs) that can ship with audio drivers, see [Windows 11 APIs for Audio Processing Objects](/windows-hardware/drivers/audio/windows-11-apis-for-audio-processing-objects).

## -see-also

