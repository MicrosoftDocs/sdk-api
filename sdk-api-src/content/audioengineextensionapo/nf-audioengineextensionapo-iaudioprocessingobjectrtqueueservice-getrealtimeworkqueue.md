---
UID: NF:audioengineextensionapo.IAudioProcessingObjectRTQueueService.GetRealTimeWorkQueue
tech.root: audio
title: IAudioProcessingObjectRTQueueService::GetRealTimeWorkQueue
ms.date: 06/19/2021
targetos: Windows
description: Gets the ID of a work queue that the APO can use to schedule tasks that need to run at a real-time priority.
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
 - IAudioProcessingObjectRTQueueService::GetRealTimeWorkQueue
f1_keywords:
 - IAudioProcessingObjectRTQueueService::GetRealTimeWorkQueue
 - audioengineextensionapo/IAudioProcessingObjectRTQueueService::GetRealTimeWorkQueue
dev_langs:
 - c++
---

## -description

Gets the ID of a work queue that the APO can use to schedule tasks that need to run at a real-time priority.

## -parameters

### -param workQueueId

A DWORD containing the work queue ID.

## -returns

Returns S_OK on success.

## -remarks

The returned work queue ID is used with the real-time work queue APIs. For more information see [rtworkq.h header](../rtworkq/index.md). 

For more information on the Windows 11 APIs for the Audio Processing Objects (APOs) that can ship with audio drivers, see [Windows 11 APIs for Audio Processing Objects](/windows-hardware/drivers/audio/windows-11-apis-for-audio-processing-objects).

## -see-also

