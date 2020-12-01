---
UID: NS:audioengineendpoint.AE_CURRENT_POSITION
title: AE_CURRENT_POSITION (audioengineendpoint.h)
description: Reports the current frame position from the device to the clients.
helpviewer_keywords: ["*PAE_CURRENT_POSITION","AE_CURRENT_POSITION","AE_CURRENT_POSITION structure [Remote Desktop Services]","PAE_CURRENT_POSITION","PAE_CURRENT_POSITION structure pointer [Remote Desktop Services]","audioengineendpoint/AE_CURRENT_POSITION","audioengineendpoint/PAE_CURRENT_POSITION","termserv.ae_current_position"]
old-location: termserv\ae_current_position.htm
tech.root: TermServ
ms.assetid: 2e239114-1af7-455a-a60f-2054b05e1414
ms.date: 12/05/2018
ms.keywords: '*PAE_CURRENT_POSITION, AE_CURRENT_POSITION, AE_CURRENT_POSITION structure [Remote Desktop Services], PAE_CURRENT_POSITION, PAE_CURRENT_POSITION structure pointer [Remote Desktop Services], audioengineendpoint/AE_CURRENT_POSITION, audioengineendpoint/PAE_CURRENT_POSITION, termserv.ae_current_position'
req.header: audioengineendpoint.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7
req.target-min-winversvr: Windows Server 2008 R2
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
req.typenames: AE_CURRENT_POSITION, *PAE_CURRENT_POSITION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - AE_CURRENT_POSITION
 - audioengineendpoint/AE_CURRENT_POSITION
 - PAE_CURRENT_POSITION
 - audioengineendpoint/PAE_CURRENT_POSITION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Audioengineendpoint.h
api_name:
 - AE_CURRENT_POSITION
---

# AE_CURRENT_POSITION structure


## -description

Reports the current frame position from the device to the clients.

## -struct-fields

### -field u64DevicePosition

The device position, in frames.

### -field u64StreamPosition

The stream position, in frames, used to determine the starting point for audio capture and the render device position relative to the stream.

### -field u64PaddingFrames

The amount of padding, in frames, between the current position and the stream fill point.

### -field hnsQPCPosition

A translated quality performance counter (QPC) timer value taken at the time that the <b>u64DevicePosition</b> member was checked.

### -field f32FramesPerSecond

The calculated data rate at the point at the time the  position was set.

### -field Flag

A value of the <a href="/windows/desktop/api/audioengineendpoint/ne-audioengineendpoint-ae_position_flags">AE_POSITION_FLAGS</a> enumeration that indicates the validity of the position information.

## -remarks

The Remote Desktop Services AudioEndpoint API is for use in Remote Desktop scenarios; it is not for client applications.

## -see-also

<a href="/windows/desktop/api/audioengineendpoint/nf-audioengineendpoint-iaudioendpointrt-getcurrentpadding">IAudioEndpointRT::GetCurrentPadding</a>



<a href="/windows/desktop/api/audioengineendpoint/nf-audioengineendpoint-iaudioinputendpointrt-getinputdatapointer">IAudioInputEndpointRT::GetInputDataPointer</a>



<a href="/windows/desktop/api/audioengineendpoint/nf-audioengineendpoint-iaudiooutputendpointrt-getoutputdatapointer">IAudioOutputEndpointRT::GetOutputDataPointer</a>