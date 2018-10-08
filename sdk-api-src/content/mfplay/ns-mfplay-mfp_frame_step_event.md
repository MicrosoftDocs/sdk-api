---
UID: NS:mfplay.MFP_FRAME_STEP_EVENT
title: MFP_FRAME_STEP_EVENT
author: windows-sdk-content
description: Event structure for the MFP_EVENT_TYPE_FRAME_STEP event.
old-location: mf\mfp_frame_step_event.htm
tech.root: medfound
ms.assetid: a395e94a-8d6d-48f5-9461-9f329af984c0
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: MFP_FRAME_STEP_EVENT, MFP_FRAME_STEP_EVENT structure [Media Foundation], mf.mfp_frame_step_event, mfplay/MFP_FRAME_STEP_EVENT
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: mfplay.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - mfplay.h
api_name:
 - MFP_FRAME_STEP_EVENT
product: Windows
targetos: Windows
req.typenames: MFP_FRAME_STEP_EVENT
req.redist: 
---

# MFP_FRAME_STEP_EVENT structure


## -description



<div class="alert"><b>Important</b>  Deprecated. This API may be removed from future releases of Windows. Applications should use the <a href="https://msdn.microsoft.com/dac99908-be90-415d-8837-2f97d573feb5">Media Session</a> for playback.</div>
<div> </div>


Event structure for the <b>MFP_EVENT_TYPE_FRAME_STEP</b> event. This event is sent when the <a href="https://msdn.microsoft.com/b7965965-2fbc-4494-9368-7d9699e4092a">IMFPMediaPlayer::FrameStep</a> method completes.


## -struct-fields




### -field header


<a href="https://msdn.microsoft.com/ed9d3790-845a-4392-b755-6a5ce6e20de5">MFP_EVENT_HEADER</a> structure that contains data common to all <a href="https://msdn.microsoft.com/fa57d465-1ee9-4f7a-9be8-66a6d73f65e8">IMFPMediaPlayer</a> events.


### -field pMediaItem

Pointer to the <a href="https://msdn.microsoft.com/2839d256-bdaf-40cf-9f9d-46f9e2ce59e8">IMFPMediaItem</a> interface of the current media item.


## -remarks



To get a pointer to this structure, cast the <i>pEventHeader</i>parameter of the <a href="https://msdn.microsoft.com/2a80a9d0-83ee-4bb0-ab2c-0f68367f3bf8">IMFPMediaPlayerCallback::OnMediaPlayerEvent</a>  method.  You can use the <a href="https://msdn.microsoft.com/3ddb2d5e-d9ef-4bfd-892e-d59f430f818a">MFP_GET_FRAME_STEP_EVENT</a> macro for this purpose.




## -see-also




<a href="https://msdn.microsoft.com/7d9d01bf-861a-4c35-93b1-dbf85cbf0a32">IMFPMediaPlayerCallback</a>



<a href="https://msdn.microsoft.com/39fdd724-13ca-48ab-8a55-93529d1da3b4">Media Foundation Structures</a>



<a href="https://msdn.microsoft.com/6f143c51-ec46-46d4-9a1e-b04fcc0d8bea">Using MFPlay for Audio/Video Playback</a>
 

 

