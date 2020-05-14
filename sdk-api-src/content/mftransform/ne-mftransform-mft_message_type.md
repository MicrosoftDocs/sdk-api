---
UID: NE:mftransform._MFT_MESSAGE_TYPE
title: MFT_MESSAGE_TYPE (mftransform.h)
description: Defines messages for a Media Foundation transform (MFT).helpviewer_keywords: ["55b0aa32-53af-4f19-9d99-9885c1e28588","MFT_MESSAGE_COMMAND_DRAIN","MFT_MESSAGE_COMMAND_FLUSH","MFT_MESSAGE_COMMAND_MARKER","MFT_MESSAGE_COMMAND_TICK","MFT_MESSAGE_DROP_SAMPLES","MFT_MESSAGE_NOTIFY_BEGIN_STREAMING","MFT_MESSAGE_NOTIFY_END_OF_STREAM","MFT_MESSAGE_NOTIFY_END_STREAMING","MFT_MESSAGE_NOTIFY_START_OF_STREAM","MFT_MESSAGE_SET_D3D_MANAGER","MFT_MESSAGE_TYPE","MFT_MESSAGE_TYPE enumeration [Media Foundation]","mf.mft_message_type","mftransform/MFT_MESSAGE_COMMAND_DRAIN","mftransform/MFT_MESSAGE_COMMAND_FLUSH","mftransform/MFT_MESSAGE_COMMAND_MARKER","mftransform/MFT_MESSAGE_COMMAND_TICK","mftransform/MFT_MESSAGE_DROP_SAMPLES","mftransform/MFT_MESSAGE_NOTIFY_BEGIN_STREAMING","mftransform/MFT_MESSAGE_NOTIFY_END_OF_STREAM","mftransform/MFT_MESSAGE_NOTIFY_END_STREAMING","mftransform/MFT_MESSAGE_NOTIFY_START_OF_STREAM","mftransform/MFT_MESSAGE_SET_D3D_MANAGER","mftransform/MFT_MESSAGE_TYPE"]
old-location: mf\mft_message_type.htm
tech.root: medfound
ms.assetid: 55b0aa32-53af-4f19-9d99-9885c1e28588
ms.date: 12/05/2018
ms.keywords: 55b0aa32-53af-4f19-9d99-9885c1e28588, MFT_MESSAGE_COMMAND_DRAIN, MFT_MESSAGE_COMMAND_FLUSH, MFT_MESSAGE_COMMAND_MARKER, MFT_MESSAGE_COMMAND_TICK, MFT_MESSAGE_DROP_SAMPLES, MFT_MESSAGE_NOTIFY_BEGIN_STREAMING, MFT_MESSAGE_NOTIFY_END_OF_STREAM, MFT_MESSAGE_NOTIFY_END_STREAMING, MFT_MESSAGE_NOTIFY_START_OF_STREAM, MFT_MESSAGE_SET_D3D_MANAGER, MFT_MESSAGE_TYPE, MFT_MESSAGE_TYPE enumeration [Media Foundation], mf.mft_message_type, mftransform/MFT_MESSAGE_COMMAND_DRAIN, mftransform/MFT_MESSAGE_COMMAND_FLUSH, mftransform/MFT_MESSAGE_COMMAND_MARKER, mftransform/MFT_MESSAGE_COMMAND_TICK, mftransform/MFT_MESSAGE_DROP_SAMPLES, mftransform/MFT_MESSAGE_NOTIFY_BEGIN_STREAMING, mftransform/MFT_MESSAGE_NOTIFY_END_OF_STREAM, mftransform/MFT_MESSAGE_NOTIFY_END_STREAMING, mftransform/MFT_MESSAGE_NOTIFY_START_OF_STREAM, mftransform/MFT_MESSAGE_SET_D3D_MANAGER, mftransform/MFT_MESSAGE_TYPE
f1_keywords:
- mftransform/MFT_MESSAGE_TYPE
dev_langs:
- c++
req.header: mftransform.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- mftransform.h
api_name:
- MFT_MESSAGE_TYPE
targetos: Windows
req.typenames: MFT_MESSAGE_TYPE
req.redist: 
ms.custom: 19H1
---

# MFT_MESSAGE_TYPE enumeration


## -description


Defines messages for a Media Foundation transform (MFT). To send a message to an MFT, call <a href="https://docs.microsoft.com/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage">IMFTransform::ProcessMessage</a>.


## -enum-fields




### -field MFT_MESSAGE_COMMAND_FLUSH

Requests the MFT to flush all stored data. 

See <a href="https://docs.microsoft.com/windows/desktop/medfound/mft-message-command-flush">MFT_MESSAGE_COMMAND_FLUSH</a>.
            
          


### -field MFT_MESSAGE_COMMAND_DRAIN

Requests the MFT to drain any stored data.

See <a href="https://docs.microsoft.com/windows/desktop/medfound/mft-message-command-drain">MFT_MESSAGE_COMMAND_DRAIN</a>.


### -field MFT_MESSAGE_SET_D3D_MANAGER

Sets or clears the <a href="https://docs.microsoft.com/windows/desktop/medfound/direct3d-device-manager">Direct3D Device Manager</a> for DirectX Video Accereration (DXVA).
            
            
          

See <a href="https://docs.microsoft.com/windows/desktop/medfound/mft-message-set-d3d-manager">MFT_MESSAGE_SET_D3D_MANAGER</a>.


### -field MFT_MESSAGE_DROP_SAMPLES

<b>Note</b> Requires Windows 7.


### -field MFT_MESSAGE_COMMAND_TICK

<b>Note</b> Requires Windows 8.


### -field MFT_MESSAGE_NOTIFY_BEGIN_STREAMING

Notifies the MFT that streaming is about to begin.
            
          

See <a href="https://docs.microsoft.com/windows/desktop/medfound/mft-message-notify-begin-streaming">MFT_MESSAGE_NOTIFY_BEGIN_STREAMING</a>.


### -field MFT_MESSAGE_NOTIFY_END_STREAMING

Notifies the MFT that streaming is about to end.
            
          

See <a href="https://docs.microsoft.com/windows/desktop/medfound/mft-message-notify-end-streaming">MFT_MESSAGE_NOTIFY_END_STREAMING</a>.


### -field MFT_MESSAGE_NOTIFY_END_OF_STREAM

Notifies the MFT that an input stream has ended.
            
          

See <a href="https://docs.microsoft.com/windows/desktop/medfound/mft-message-notify-end-of-stream">MFT_MESSAGE_NOTIFY_END_OF_STREAM</a>.


### -field MFT_MESSAGE_NOTIFY_START_OF_STREAM

Notifies the MFT that the first sample is about to be processed. 

See
            
           <a href="https://docs.microsoft.com/windows/desktop/medfound/mft-message-notify-start-of-stream">MFT_MESSAGE_NOTIFY_START_OF_STREAM</a>.


### -field MFT_MESSAGE_NOTIFY_RELEASE_RESOURCES


### -field MFT_MESSAGE_NOTIFY_REACQUIRE_RESOURCES


### -field MFT_MESSAGE_NOTIFY_EVENT


### -field MFT_MESSAGE_COMMAND_SET_OUTPUT_STREAM_STATE


### -field MFT_MESSAGE_COMMAND_FLUSH_OUTPUT_STREAM


### -field MFT_MESSAGE_COMMAND_MARKER

Marks a point in the stream. This message applies only to asynchronous MFTs. 

See <a href="https://docs.microsoft.com/windows/desktop/medfound/mft-message-command-marker">MFT_MESSAGE_COMMAND_MARKER</a>.

<div class="alert"><b>Note</b>  Requires Windows 7</div>
<div> </div>

## -remarks



Some messages require specific actions from the MFT. These events have "MESSAGE" in the message name. Other messages are informational; they notify the MFT of some action by the client, and do not require any particular response from the MFT. These messages have "NOTIFY" in the messages name. Except where noted, an MFT should not rely on the client sending notification messages.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage">IMFTransform::ProcessMessage</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-enumerations">Media Foundation Enumerations</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-transforms">Media Foundation Transforms</a>
 

 

