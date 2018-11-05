---
UID: NE:mftransform._MFT_MESSAGE_TYPE
title: "_MFT_MESSAGE_TYPE"
author: windows-sdk-content
description: Defines messages for a Media Foundation transform (MFT).
old-location: mf\mft_message_type.htm
tech.root: medfound
ms.assetid: 55b0aa32-53af-4f19-9d99-9885c1e28588
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: 55b0aa32-53af-4f19-9d99-9885c1e28588, MFT_MESSAGE_COMMAND_DRAIN, MFT_MESSAGE_COMMAND_FLUSH, MFT_MESSAGE_COMMAND_MARKER, MFT_MESSAGE_COMMAND_TICK, MFT_MESSAGE_DROP_SAMPLES, MFT_MESSAGE_NOTIFY_BEGIN_STREAMING, MFT_MESSAGE_NOTIFY_END_OF_STREAM, MFT_MESSAGE_NOTIFY_END_STREAMING, MFT_MESSAGE_NOTIFY_START_OF_STREAM, MFT_MESSAGE_SET_D3D_MANAGER, MFT_MESSAGE_TYPE, MFT_MESSAGE_TYPE enumeration [Media Foundation], _MFT_MESSAGE_TYPE, mf.mft_message_type, mftransform/MFT_MESSAGE_COMMAND_DRAIN, mftransform/MFT_MESSAGE_COMMAND_FLUSH, mftransform/MFT_MESSAGE_COMMAND_MARKER, mftransform/MFT_MESSAGE_COMMAND_TICK, mftransform/MFT_MESSAGE_DROP_SAMPLES, mftransform/MFT_MESSAGE_NOTIFY_BEGIN_STREAMING, mftransform/MFT_MESSAGE_NOTIFY_END_OF_STREAM, mftransform/MFT_MESSAGE_NOTIFY_END_STREAMING, mftransform/MFT_MESSAGE_NOTIFY_START_OF_STREAM, mftransform/MFT_MESSAGE_SET_D3D_MANAGER, mftransform/MFT_MESSAGE_TYPE
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
product: Windows
targetos: Windows
req.typenames: MFT_MESSAGE_TYPE
req.redist: 
---

# _MFT_MESSAGE_TYPE enumeration


## -description


Defines messages for a Media Foundation transform (MFT). To send a message to an MFT, call <a href="https://msdn.microsoft.com/a6dc67e5-8473-444a-8463-24f411e59565">IMFTransform::ProcessMessage</a>.


## -enum-fields




### -field MFT_MESSAGE_COMMAND_FLUSH

Requests the MFT to flush all stored data. 

See <a href="https://msdn.microsoft.com/c799a962-da79-46df-a37f-4016c8c1701e">MFT_MESSAGE_COMMAND_FLUSH</a>.
            
          


### -field MFT_MESSAGE_COMMAND_DRAIN

Requests the MFT to drain any stored data.

See <a href="https://msdn.microsoft.com/c48f3a88-a007-4f30-ac60-9e5a8c24e1ee">MFT_MESSAGE_COMMAND_DRAIN</a>.


### -field MFT_MESSAGE_SET_D3D_MANAGER

Sets or clears the <a href="https://msdn.microsoft.com/d82fd82d-510e-4004-b18b-8f2372e29701">Direct3D Device Manager</a> for DirectX Video Accereration (DXVA).
            
            
          

See <a href="https://msdn.microsoft.com/fd346d56-1f80-488a-94c8-4e4e36d72890">MFT_MESSAGE_SET_D3D_MANAGER</a>.


### -field MFT_MESSAGE_DROP_SAMPLES

<b>Note</b> Requires Windows 7.


### -field MFT_MESSAGE_COMMAND_TICK

<b>Note</b> Requires Windows 8.


### -field MFT_MESSAGE_NOTIFY_BEGIN_STREAMING

Notifies the MFT that streaming is about to begin.
            
          

See <a href="https://msdn.microsoft.com/a7f02e92-a747-4ac6-aa83-60897acb2bc5">MFT_MESSAGE_NOTIFY_BEGIN_STREAMING</a>.


### -field MFT_MESSAGE_NOTIFY_END_STREAMING

Notifies the MFT that streaming is about to end.
            
          

See <a href="https://msdn.microsoft.com/df313a66-e80f-499c-a9f2-a7cbaaf0a7d4">MFT_MESSAGE_NOTIFY_END_STREAMING</a>.


### -field MFT_MESSAGE_NOTIFY_END_OF_STREAM

Notifies the MFT that an input stream has ended.
            
          

See <a href="https://msdn.microsoft.com/2d6cdf45-1bb4-4915-bd27-efa041089100">MFT_MESSAGE_NOTIFY_END_OF_STREAM</a>.


### -field MFT_MESSAGE_NOTIFY_START_OF_STREAM

Notifies the MFT that the first sample is about to be processed. 

See
            
           <a href="https://msdn.microsoft.com/579df695-02c4-4332-b1b4-c7bd9da50c0f">MFT_MESSAGE_NOTIFY_START_OF_STREAM</a>.


### -field MFT_MESSAGE_NOTIFY_RELEASE_RESOURCES


### -field MFT_MESSAGE_NOTIFY_REACQUIRE_RESOURCES


### -field MFT_MESSAGE_NOTIFY_EVENT


### -field MFT_MESSAGE_COMMAND_SET_OUTPUT_STREAM_STATE


### -field MFT_MESSAGE_COMMAND_FLUSH_OUTPUT_STREAM


### -field MFT_MESSAGE_COMMAND_MARKER

Marks a point in the stream. This message applies only to asynchronous MFTs. 

See <a href="https://msdn.microsoft.com/eae1d066-64af-45e2-b8bb-eddf9147ad8b">MFT_MESSAGE_COMMAND_MARKER</a>.

<div class="alert"><b>Note</b>  Requires Windows 7</div>
<div> </div>

## -remarks



Some messages require specific actions from the MFT. These events have "MESSAGE" in the message name. Other messages are informational; they notify the MFT of some action by the client, and do not require any particular response from the MFT. These messages have "NOTIFY" in the messages name. Except where noted, an MFT should not rely on the client sending notification messages.




## -see-also




<a href="https://msdn.microsoft.com/a6dc67e5-8473-444a-8463-24f411e59565">IMFTransform::ProcessMessage</a>



<a href="https://msdn.microsoft.com/f26a730f-18c4-4247-acaf-af1dfad19086">Media Foundation Enumerations</a>



<a href="https://msdn.microsoft.com/cb23fe0a-c42c-4912-a0bf-1f0b18a6f4e0">Media Foundation Transforms</a>
 

 

