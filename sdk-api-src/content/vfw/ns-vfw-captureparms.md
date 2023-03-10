---
UID: NS:vfw.tagCaptureParms
title: CAPTUREPARMS (vfw.h)
description: The CAPTUREPARMS structure contains parameters that control the streaming video capture process. This structure is used to get and set parameters that affect the capture rate, the number of buffers to use while capturing, and how capture is terminated.
helpviewer_keywords: ["*LPCAPTUREPARMS","*PCAPTUREPARMS","CAPTUREPARMS","CAPTUREPARMS structure [Windows Multimedia]","_win32_CAPTUREPARMS_str","multimedia.captureparms","vfw/CAPTUREPARMS"]
old-location: multimedia\captureparms.htm
tech.root: Multimedia
ms.assetid: 6bf7e374-5991-4a7b-984a-628d3e77b2d7
ms.date: 12/05/2018
ms.keywords: '*LPCAPTUREPARMS, *PCAPTUREPARMS, CAPTUREPARMS, CAPTUREPARMS structure [Windows Multimedia], _win32_CAPTUREPARMS_str, multimedia.captureparms, vfw/CAPTUREPARMS'
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
req.typenames: CAPTUREPARMS, *PCAPTUREPARMS, *LPCAPTUREPARMS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagCaptureParms
 - vfw/tagCaptureParms
 - PCAPTUREPARMS
 - vfw/PCAPTUREPARMS
 - CAPTUREPARMS
 - vfw/CAPTUREPARMS
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
 - CAPTUREPARMS
---

# CAPTUREPARMS structure


## -description

The <b>CAPTUREPARMS</b> structure contains parameters that control the streaming video capture process. This structure is used to get and set parameters that affect the capture rate, the number of buffers to use while capturing, and how capture is terminated.

## -struct-fields

### -field dwRequestMicroSecPerFrame

Requested frame rate, in microseconds. The default value is 66667, which corresponds to 15 frames per second.

### -field fMakeUserHitOKToCapture

User-initiated capture flag. If this member is <b>TRUE</b>, AVICap displays a dialog box prompting the user to initiate capture. The default value is <b>FALSE</b>.

### -field wPercentDropForError

Maximum allowable percentage of dropped frames during capture. Values range from 0 to 100. The default value is 10.

### -field fYield

Yield flag. If this member is <b>TRUE</b>, the capture window spawns a separate background thread to perform step and streaming capture. The default value is <b>FALSE</b>.

Applications that set this flag must handle potential reentry issues because the controls in the application are not disabled while capture is in progress.

### -field dwIndexSize

Maximum number of index entries in an AVI file. Values range from 1800 to 324,000. If set to 0, a default value of 34,952 (32K frames plus a proportional number of audio buffers) is used.

Each video frame or buffer of waveform-audio data uses one index entry. The value of this entry establishes a limit for the number of frames or audio buffers that can be captured.

### -field wChunkGranularity

Logical block size, in bytes, of an AVI file. The value 0 indicates the current sector size is used as the granularity.

### -field fUsingDOSMemory

Not used in Win32 applications.

### -field wNumVideoRequested

Maximum number of video buffers to allocate. The memory area to place the buffers is specified with <b>fUsingDOSMemory</b>. The actual number of buffers allocated might be lower if memory is unavailable.

### -field fCaptureAudio

Capture audio flag. If this member is <b>TRUE</b>, audio is captured during streaming capture. This is the default value if audio hardware is installed.

### -field wNumAudioRequested

Maximum number of audio buffers to allocate. The maximum number of buffers is 10.

### -field vKeyAbort

Virtual keycode used to terminate streaming capture. The default value is VK_ESCAPE. You must call the <a href="/windows/win32/api/winuser/nf-winuser-registerhotkey">RegisterHotKey</a> function before specifying a keystroke that can abort a capture session.

You can combine keycodes that include CTRL and SHIFT keystrokes by using the logical OR operator with the keycodes for CTRL (0x8000) and SHIFT (0x4000).

### -field fAbortLeftMouse

Abort flag for left mouse button. If this member is <b>TRUE</b>, streaming capture stops if the left mouse button is pressed. The default value is <b>TRUE</b>.

### -field fAbortRightMouse

Abort flag for right mouse button. If this member is <b>TRUE</b>, streaming capture stops if the right mouse button is pressed. The default value is <b>TRUE</b>.

### -field fLimitEnabled

Time limit enabled flag. If this member is <b>TRUE</b>, streaming capture stops after the number of seconds in <b>wTimeLimit</b> has elapsed. The default value is <b>FALSE</b>.

### -field wTimeLimit

Time limit for capture, in seconds. This parameter is used only if <b>fLimitEnabled</b> is <b>TRUE</b>.

### -field fMCIControl

MCI device capture flag. If this member is <b>TRUE</b>, AVICap controls an MCI-compatible video source during streaming capture. MCI-compatible video sources include VCRs and laserdiscs.

### -field fStepMCIDevice

MCI device step capture flag. If this member is <b>TRUE</b>, step capture using an MCI device as a video source is enabled. If it is <b>FALSE</b>, real-time capture using an MCI device is enabled. (If <b>fMCIControl</b> is <b>FALSE</b>, this member is ignored.)

### -field dwMCIStartTime

Starting position, in milliseconds, of the MCI device for the capture sequence. (If <b>fMCIControl</b> is <b>FALSE</b>, this member is ignored.)

### -field dwMCIStopTime

Stopping position, in milliseconds, of the MCI device for the capture sequence. When this position in the content is reached, capture ends and the MCI device stops. (If <b>fMCIControl</b> is <b>FALSE</b>, this member is ignored.)

### -field fStepCaptureAt2x

Double-resolution step capture flag. If this member is <b>TRUE</b>, the capture hardware captures at twice the specified resolution. (The resolution for the height and width is doubled.)

Enable this option if the hardware does not support hardware-based decimation and you are capturing in the RGB format.

### -field wStepCaptureAverageFrames

Number of times a frame is sampled when creating a frame based on the average sample. A typical value for the number of averages is 5.

### -field dwAudioBufferSize

Audio buffer size. If the default value of zero is used, the size of each buffer will be the maximum of 0.5 seconds of audio or 10K bytes.

### -field fDisableWriteCache

Not used in Win32 applications.

### -field AVStreamMaster

Indicates whether the audio stream controls the clock when writing an AVI file. If this member is set to AVSTREAMMASTER_AUDIO, the audio stream is considered the master stream and the video stream duration is forced to match the audio duration. If this member is set to AVSTREAMMASTER_NONE, the durations of audio and video streams can differ.

## -remarks

The WM_CAP_GET_SEQUENCE_SETUP message or <a href="/windows/desktop/api/vfw/nf-vfw-capcapturegetsetup">capCaptureGetSetup</a> macro is used to retrieve the current capture parameters. The WM_CAP_SET_SEQUENCE_SETUP message or <a href="/windows/desktop/api/vfw/nf-vfw-capcapturesetsetup">capCaptureSetSetup</a> macro is used to set the capture parameters.

The <a href="/windows/desktop/Multimedia/wm-cap-get-sequence-setup">WM_CAP_GET_SEQUENCE_SETUP</a> message or <a href="/windows/desktop/api/vfw/nf-vfw-capcapturegetsetup">capCaptureGetSetup</a> macro is used to retrieve the current capture parameters. The <a href="/windows/desktop/Multimedia/wm-cap-set-sequence-setup">WM_CAP_SET_SEQUENCE_SETUP</a> message or <a href="/windows/desktop/api/vfw/nf-vfw-capcapturesetsetup">capCaptureSetSetup</a> macro is used to set the capture parameters.

## -see-also

<a href="/windows/win32/api/winuser/nf-winuser-registerhotkey">RegisterHotKey</a>



Video Capture



<a href="/windows/desktop/Multimedia/video-capture-structures">Video Capture Structures</a>



<a href="/windows/desktop/Multimedia/wm-cap-get-sequence-setup">WM_CAP_GET_SEQUENCE_SETUP</a>



<a href="/windows/desktop/Multimedia/wm-cap-set-sequence-setup">WM_CAP_SET_SEQUENCE_SETUP</a>



<a href="/windows/desktop/api/vfw/nf-vfw-capcapturegetsetup">capCaptureGetSetup</a>



<a href="/windows/desktop/api/vfw/nf-vfw-capcapturesetsetup">capCaptureSetSetup</a>