---
UID: NF:vfw.MCIWndRecord
title: MCIWndRecord macro (vfw.h)
description: The MCIWndRecord macro begins recording content using the MCI device. The recording process begins at the current position in the content and will overwrite existing data for the duration of the recording.
helpviewer_keywords: ["MCIWndRecord","MCIWndRecord macro [Windows Multimedia]","_win32_MCIWndRecord","multimedia.mciwndrecord","vfw/MCIWndRecord"]
old-location: multimedia\mciwndrecord.htm
tech.root: Multimedia
ms.assetid: 9f68f258-6e7d-45f0-8b42-93a03d559c04
ms.date: 07/01/2025
ms.keywords: MCIWndRecord, MCIWndRecord macro [Windows Multimedia], _win32_MCIWndRecord, multimedia.mciwndrecord, vfw/MCIWndRecord
req.header: vfw.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MCIWndRecord
 - vfw/MCIWndRecord
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Vfw.h
api_name:
 - MCIWndRecord
---

# MCIWndRecord macro

## -syntax

```cpp
LONG MCIWndRecord(
     hwnd
);
```

## -returns

Type: **LONG**

Returns zero if successful or an error otherwise.


## -description

The <b>MCIWndRecord</b> macro begins recording content using the MCI device. The recording process begins at the current position in the content and will overwrite existing data for the duration of the recording.

## -parameters

### -param hwnd

Handle of the MCIWnd window.

## -remarks

The function that an MCI device performs during recording depends on the characteristics of the device. An MCI device that uses files, such as a waveform-audio device, sends data to the file during recording. An MCI device that does not use files, such as a video-cassette recorder, receives and externally records data on another medium.

