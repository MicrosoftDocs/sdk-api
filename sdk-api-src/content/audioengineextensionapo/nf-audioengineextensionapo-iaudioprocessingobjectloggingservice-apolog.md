---
UID: NF:audioengineextensionapo.IAudioProcessingObjectLoggingService.ApoLog
tech.root: audio
title: IAudioProcessingObjectLoggingService::ApoLog
ms.date: 06/19/2021
targetos: Windows
description: Logs an APO event.
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: audioengineextensionapo.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows Build 22000
req.target-min-winversvr: 
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - audioengineextensionapo.h
api_name:
 - IAudioProcessingObjectLoggingService::ApoLog
f1_keywords:
 - IAudioProcessingObjectLoggingService::ApoLog
 - audioengineextensionapo/IAudioProcessingObjectLoggingService::ApoLog
dev_langs:
 - c++
---

## -description

Logs an APO event.

## -parameters

### -param level

A value from the [APO_LOG_LEVEL](ne-audioengineextensionapo-apo_log_level.md) enumeration specifying the level of the event being logged.

### -param format

The format-control string for the log message.

### -param ...

Format argument list.

## -remarks

> [!NOTE] 
> This method should never be called from a real-time priority thread. For more information on thread priorities, see [Scheduling Priorities](/windows/win32/procthread/scheduling-priorities).

For more information on the Windows 11 APIs for the Audio Processing Objects (APOs) that can ship with audio drivers, see [Windows 11 APIs for Audio Processing Objects](/windows-hardware/drivers/audio/windows-11-apis-for-audio-processing-objects).

## -see-also

