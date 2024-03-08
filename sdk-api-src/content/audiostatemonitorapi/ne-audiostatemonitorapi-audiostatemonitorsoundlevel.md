---
UID: NE:audiostatemonitorapi.AudioStateMonitorSoundLevel
tech.root: CoreAudio
title: AudioStateMonitorSoundLevel
ms.date: 06/21/2023
targetos: Windows
description: 
prerelease: false
req.construct-type: enumeration
req.ddi-compliance: 
req.header: audiostatemonitorapi.h
req.include-header: 
req.kmdf-ver: 
req.max-support: 
req.target-min-winverclnt: Windows build 19043
req.target-min-winversvr: 
req.target-type: 
req.typenames: 
typedef_isUnnamed: false
req.umdf-ver: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - audiostatemonitorapi.h
api_name:
 - AudioStateMonitorSoundLevel
f1_keywords:
 - AudioStateMonitorSoundLevel
 - audiostatemonitorapi/AudioStateMonitorSoundLevel
dev_langs:
 - c++
helpviewer_keywords:
 - AudioStateMonitorSoundLevel
---

## -description

Specifies a sound level for audio streams being queried with a call to [IAudioStateMonitor::GetSoundLevel](nf-audiostatemonitorapi-iaudiostatemonitor-getsoundlevel.md)

## -enum-fields

### -field Muted

The audio is muted.

### -field Low

The audio level is low.

### -field Full

The audio level is full.

## -remarks

## -see-also

