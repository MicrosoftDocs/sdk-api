---
UID: NS:vfw.tagCaptureParms
title: tagCaptureParms
author: windows-sdk-content
description: The CAPTUREPARMS structure contains parameters that control the streaming video capture process. This structure is used to get and set parameters that affect the capture rate, the number of buffers to use while capturing, and how capture is terminated.
old-location: multimedia\captureparms.htm
old-project: Multimedia
ms.assetid: 6bf7e374-5991-4a7b-984a-628d3e77b2d7
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*LPCAPTUREPARMS, *PCAPTUREPARMS, CAPTUREPARMS, CAPTUREPARMS structure [Windows Multimedia], _win32_CAPTUREPARMS_str, multimedia.captureparms, tagCaptureParms, vfw/CAPTUREPARMS"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: vfw.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: CAPTUREPARMS, *PCAPTUREPARMS, *LPCAPTUREPARMS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Vfw.h
api_name:
 - CAPTUREPARMS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# tagCaptureParms structure


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

Virtual keycode used to terminate streaming capture. The default value is VK_ESCAPE. You must call the <a href="http://go.microsoft.com/fwlink/p/?linkid=16996">RegisterHotKey</a> function before specifying a keystroke that can abort a capture session.

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



The WM_CAP_GET_SEQUENCE_SETUP message or <a href="https://msdn.microsoft.com/198b1aae-b719-4fb8-a11d-859eaf7a4606">capCaptureGetSetup</a> macro is used to retrieve the current capture parameters. The WM_CAP_SET_SEQUENCE_SETUP message or <a href="https://msdn.microsoft.com/663dcb34-6b11-4208-b5d6-216799fb774d">capCaptureSetSetup</a> macro is used to set the capture parameters.

The <a href="https://msdn.microsoft.com/2220c92a-1994-4f15-9730-1cf01972dda6">WM_CAP_GET_SEQUENCE_SETUP</a> message or <a href="https://msdn.microsoft.com/198b1aae-b719-4fb8-a11d-859eaf7a4606">capCaptureGetSetup</a> macro is used to retrieve the current capture parameters. The <a href="https://msdn.microsoft.com/ba9adb26-6627-469b-a836-f4f277ddb7c4">WM_CAP_SET_SEQUENCE_SETUP</a> message or <a href="https://msdn.microsoft.com/663dcb34-6b11-4208-b5d6-216799fb774d">capCaptureSetSetup</a> macro is used to set the capture parameters.




## -see-also




<a href="http://go.microsoft.com/fwlink/p/?linkid=16996">RegisterHotKey</a>



Video Capture



<a href="https://msdn.microsoft.com/180010d2-240e-433d-b306-341b9b1e0b57">Video Capture Structures</a>



<a href="https://msdn.microsoft.com/2220c92a-1994-4f15-9730-1cf01972dda6">WM_CAP_GET_SEQUENCE_SETUP</a>



<a href="https://msdn.microsoft.com/ba9adb26-6627-469b-a836-f4f277ddb7c4">WM_CAP_SET_SEQUENCE_SETUP</a>



<a href="https://msdn.microsoft.com/198b1aae-b719-4fb8-a11d-859eaf7a4606">capCaptureGetSetup</a>



<a href="https://msdn.microsoft.com/663dcb34-6b11-4208-b5d6-216799fb774d">capCaptureSetSetup</a>
 

 

