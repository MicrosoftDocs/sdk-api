---
UID: NS:vfw.tagCapStatus
title: CAPSTATUS (vfw.h)
description: The CAPSTATUS structure defines the current state of the capture window.
helpviewer_keywords: ["*LPCAPSTATUS","*PCAPSTATUS","CAPSTATUS","CAPSTATUS structure [Windows Multimedia]","_win32_CAPSTATUS_str","multimedia.capstatus","vfw/CAPSTATUS"]
old-location: multimedia\capstatus.htm
tech.root: Multimedia
ms.assetid: 65ad6e33-c601-4026-a5a4-2c68576d7ab7
ms.date: 12/05/2018
ms.keywords: '*LPCAPSTATUS, *PCAPSTATUS, CAPSTATUS, CAPSTATUS structure [Windows Multimedia], _win32_CAPSTATUS_str, multimedia.capstatus, vfw/CAPSTATUS'
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
req.typenames: CAPSTATUS, *PCAPSTATUS, *LPCAPSTATUS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagCapStatus
 - vfw/tagCapStatus
 - PCAPSTATUS
 - vfw/PCAPSTATUS
 - CAPSTATUS
 - vfw/CAPSTATUS
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
 - CAPSTATUS
---

# CAPSTATUS structure


## -description

The <b>CAPSTATUS</b> structure defines the current state of the capture window.

## -struct-fields

### -field uiImageWidth

Image width, in pixels.

### -field uiImageHeight

Image height, in pixels

### -field fLiveWindow

Live window flag. The value of this member is <b>TRUE</b> if the window is displaying video using the preview method.

### -field fOverlayWindow

Overlay window flag. The value of this member is <b>TRUE</b> if the window is displaying video using hardware overlay.

### -field fScale

Input scaling flag. The value of this member is <b>TRUE</b> if the window is scaling the input video to the client area when displaying video using preview. This parameter has no effect when displaying video using overlay.

### -field ptScroll

The x- and y-offset of the pixel displayed in the upper left corner of the client area of the window.

### -field fUsingDefaultPalette

Default palette flag. The value of this member is <b>TRUE</b> if the capture driver is using its default palette.

### -field fAudioHardware

Audio hardware flag. The value of this member is <b>TRUE</b> if the system has waveform-audio hardware installed.

### -field fCapFileExists

Capture file flag. The value of this member is <b>TRUE</b> if a valid capture file has been generated.

### -field dwCurrentVideoFrame

Number of frames processed during the current (or most recent) streaming capture. This count includes dropped frames.

### -field dwCurrentVideoFramesDropped

Number of frames dropped during the current (or most recent) streaming capture. Dropped frames occur when the capture rate exceeds the rate at which frames can be saved to file. In this case, the capture driver has no buffers available for storing data. Dropping frames does not affect synchronization because the previous frame is displayed in place of the dropped frame.

### -field dwCurrentWaveSamples

Number of waveform-audio samples processed during the current (or most recent) streaming capture.

### -field dwCurrentTimeElapsedMS

Time, in milliseconds, since the start of the current (or most recent) streaming capture.

### -field hPalCurrent

Handle to current palette.

### -field fCapturingNow

Capturing flag. The value of this member is <b>TRUE</b> when capturing is in progress.

### -field dwReturn

Error return values. Use this member if your application does not support an error callback function.

### -field wNumVideoAllocated

Number of video buffers allocated. This value might be less than the number specified in the <b>wNumVideoRequested</b> member of the <a href="/windows/desktop/api/vfw/ns-vfw-captureparms">CAPTUREPARMS</a> structure.

### -field wNumAudioAllocated

Number of audio buffers allocated. This value might be less than the number specified in the <b>wNumAudioRequested</b> member of the <a href="/windows/desktop/api/vfw/ns-vfw-captureparms">CAPTUREPARMS</a> structure.

## -remarks

Because the state of a capture window changes in response to various messages, an application should update the information in this structure whenever it needs to enable menu items, determine the actual state of the capture window, or call the video format dialog box. If the application yields during streaming capture, this structure returns the progress of the capture in the <b>dwCurrentVideoFrame</b>, <b>dwCurrentVideoFramesDropped</b>, <b>dwCurrentWaveSamples</b>, and <b>dwCurrentTimeElapsedMS</b> members. Use the <a href="/windows/desktop/Multimedia/wm-cap-get-status">WM_CAP_GET_STATUS</a> message or <a href="/windows/desktop/api/vfw/nf-vfw-capgetstatus">capGetStatus</a> macro to update the contents of this structure.

## -see-also

<a href="/windows/desktop/api/vfw/ns-vfw-captureparms">CAPTUREPARMS</a>



Video Capture



<a href="/windows/desktop/Multimedia/video-capture-structures">Video Capture Structures</a>



<a href="/windows/desktop/Multimedia/wm-cap-get-status">WM_CAP_GET_STATUS</a>