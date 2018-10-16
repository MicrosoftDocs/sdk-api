---
UID: NE:mfplay.MFP_EVENT_TYPE
title: MFP_EVENT_TYPE
author: windows-sdk-content
description: Defines event types for the IMFPMediaPlayerCallback interface.
old-location: mf\mfp_event_type.htm
tech.root: medfound
ms.assetid: 95beb13d-db84-4713-9c27-27b37eac7f2f
ms.author: windowssdkdev
ms.date: 10/15/2018
ms.keywords: MFP_EVENT_TYPE, MFP_EVENT_TYPE enumeration [Media Foundation], MFP_EVENT_TYPE_ACQUIRE_USER_CREDENTIAL, MFP_EVENT_TYPE_ERROR, MFP_EVENT_TYPE_FRAME_STEP, MFP_EVENT_TYPE_MEDIAITEM_CLEARED, MFP_EVENT_TYPE_MEDIAITEM_CREATED, MFP_EVENT_TYPE_MEDIAITEM_SET, MFP_EVENT_TYPE_MF, MFP_EVENT_TYPE_PAUSE, MFP_EVENT_TYPE_PLAY, MFP_EVENT_TYPE_PLAYBACK_ENDED, MFP_EVENT_TYPE_POSITION_SET, MFP_EVENT_TYPE_RATE_SET, MFP_EVENT_TYPE_STOP, mf.mfp_event_type, mfplay/MFP_EVENT_TYPE, mfplay/MFP_EVENT_TYPE_ACQUIRE_USER_CREDENTIAL, mfplay/MFP_EVENT_TYPE_ERROR, mfplay/MFP_EVENT_TYPE_FRAME_STEP, mfplay/MFP_EVENT_TYPE_MEDIAITEM_CLEARED, mfplay/MFP_EVENT_TYPE_MEDIAITEM_CREATED, mfplay/MFP_EVENT_TYPE_MEDIAITEM_SET, mfplay/MFP_EVENT_TYPE_MF, mfplay/MFP_EVENT_TYPE_PAUSE, mfplay/MFP_EVENT_TYPE_PLAY, mfplay/MFP_EVENT_TYPE_PLAYBACK_ENDED, mfplay/MFP_EVENT_TYPE_POSITION_SET, mfplay/MFP_EVENT_TYPE_RATE_SET, mfplay/MFP_EVENT_TYPE_STOP
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
 - MFP_EVENT_TYPE
product: Windows
targetos: Windows
req.typenames: MFP_EVENT_TYPE
req.redist: 
---

# MFP_EVENT_TYPE enumeration


## -description



<div class="alert"><b>Important</b>  Deprecated. This API may be removed from future releases of Windows. Applications should use the <a href="https://msdn.microsoft.com/dac99908-be90-415d-8837-2f97d573feb5">Media Session</a> for playback.</div>
<div> </div>


Defines event types for the <a href="https://msdn.microsoft.com/7d9d01bf-861a-4c35-93b1-dbf85cbf0a32">IMFPMediaPlayerCallback</a> interface.


## -enum-fields




### -field MFP_EVENT_TYPE_PLAY

Playback has started. This event is sent when the <a href="https://msdn.microsoft.com/24d6e8a0-d910-46f9-8172-dfcb68c4f364">IMFPMediaPlayer::Play</a> method completes.


### -field MFP_EVENT_TYPE_PAUSE

Playback has paused. This event is sent when the <a href="https://msdn.microsoft.com/f6bf6896-6ed6-4135-a01d-f875bfdc72f4">IMFPMediaPlayer::Pause</a> method completes.


### -field MFP_EVENT_TYPE_STOP

Playback has stopped. This event is sent when the <a href="https://msdn.microsoft.com/1cfa41c7-209e-4c18-a204-563ede29c7c6">IMFPMediaPlayer::Stop</a> method completes.


### -field MFP_EVENT_TYPE_POSITION_SET

The MFPlay player object has seeked to a new playback position. This event is sent when the <a href="https://msdn.microsoft.com/d8665c3b-e0da-4a6f-a61b-38d507d1e78a">IMFPMediaPlayer::SetPosition</a> method completes.


### -field MFP_EVENT_TYPE_RATE_SET

The playback rate has changed. This event is sent when the <a href="https://msdn.microsoft.com/7e9d4a0d-b61f-47d9-af47-d8a07cd728f6">IMFPMediaPlayer::SetRate</a> method completes.


### -field MFP_EVENT_TYPE_MEDIAITEM_CREATED

A new media item was created. This event is sent when the <a href="https://msdn.microsoft.com/7dc2a7f3-81b4-46c6-b45e-44c6a20afc6b">IMFPMediaPlayer::CreateMediaItemFromURL</a> or <a href="https://msdn.microsoft.com/d647df89-b874-448e-ae41-ee3bcb55521f">CreateMediaItemFromObject</a> method completes. 


### -field MFP_EVENT_TYPE_MEDIAITEM_SET

A media item is ready for playback. This event is sent when the <a href="https://msdn.microsoft.com/c792a024-c4f8-4e0b-9720-259d1dc28ee8">IMFPMediaPlayer::SetMediaItem</a> method completes.


### -field MFP_EVENT_TYPE_FRAME_STEP

A frame-step operation has completed. This event is sent when the <a href="https://msdn.microsoft.com/b7965965-2fbc-4494-9368-7d9699e4092a">IMFPMediaPlayer::FrameStep</a> method completes.


### -field MFP_EVENT_TYPE_MEDIAITEM_CLEARED

The current media item was cleared. This event is sent when the <a href="https://msdn.microsoft.com/2c2b23ab-b282-445f-a5a0-4291ee6f22ba">IMFPMediaPlayer::ClearMediaItem</a> method completes.


### -field MFP_EVENT_TYPE_MF

A pipeline object sent an event. The player object forwards certain pipeline events to the application. For more information, see <a href="https://msdn.microsoft.com/61dec86d-919c-4b1b-ab2a-527d062ae0f8">MFP_MF_EVENT</a>.


### -field MFP_EVENT_TYPE_ERROR

A playback error has occurred. 


### -field MFP_EVENT_TYPE_PLAYBACK_ENDED

Playback has ended. The player object sends this event when playback reaches the end of the media file.


### -field MFP_EVENT_TYPE_ACQUIRE_USER_CREDENTIAL

The media source requires authentication before it can play the file.


## -remarks



For each event type, the <a href="https://msdn.microsoft.com/2a80a9d0-83ee-4bb0-ab2c-0f68367f3bf8">IMFPMediaPlayerCallback::OnMediaPlayerEvent</a> callback receives a pointer to a data structure. The first part of the data structure is always an <a href="https://msdn.microsoft.com/ed9d3790-845a-4392-b755-6a5ce6e20de5">MFP_EVENT_HEADER</a> structure. The following table lists the data structure for each event type.

In your implementation of <a href="https://msdn.microsoft.com/2a80a9d0-83ee-4bb0-ab2c-0f68367f3bf8">OnMediaPlayerEvent</a>, you must cast the <i>pEventHeader</i> parameter to the correct structure type. A set of macros is defined for this purpose. These macros check the value of the event type and return <b>NULL</b> if there is a mismatch; otherwise they return a pointer to the correct structure type.

<table>
<tr>
<td><b>Event type</b></td>
<td>
<b>Event structure</b>

<b>Pointer cast macro</b>

</td>
</tr>
<tr>
<td>MFP_EVENT_TYPE_PLAY</td>
<td>

<a href="https://msdn.microsoft.com/2cf8805f-8a3c-45a6-87ad-fa4da9115833">MFP_PLAY_EVENT</a>



<a href="https://msdn.microsoft.com/2a67965f-3429-4ce7-ae62-8952cacb00eb">MFP_GET_PLAY_EVENT</a>


</td>
</tr>
<tr>
<td>MFP_EVENT_TYPE_PAUSE</td>
<td>

<a href="https://msdn.microsoft.com/8475dca1-2ecd-49dc-97b6-bb2823286c04">MFP_PAUSE_EVENT</a>



<a href="https://msdn.microsoft.com/492b8c37-eae0-42ea-9a62-3c2e3ee0233f">MFP_GET_PAUSE_EVENT</a>


</td>
</tr>
<tr>
<td>MFP_EVENT_TYPE_STOP</td>
<td>

<a href="https://msdn.microsoft.com/67459c57-7912-4c51-9d76-3dc98f0e65ba">MFP_STOP_EVENT</a>



<a href="https://msdn.microsoft.com/3ca3fa23-1abf-49fc-96e3-f094b483c78f">MFP_GET_STOP_EVENT</a>


</td>
</tr>
<tr>
<td>MFP_EVENT_TYPE_POSITION_SET</td>
<td>

<a href="https://msdn.microsoft.com/5a40f12b-c463-4c07-b062-411c0701254f">MFP_POSITION_SET_EVENT</a>



<a href="https://msdn.microsoft.com/e9b692e6-7b7c-45ac-bbaa-7060578f9403">MFP_GET_POSITION_SET_EVENT</a>


</td>
</tr>
<tr>
<td>MFP_EVENT_TYPE_RATE_SET</td>
<td>

<a href="https://msdn.microsoft.com/19e3bcb0-340a-46dc-bfda-62890ec9a8ae">MFP_RATE_SET_EVENT</a>



<a href="https://msdn.microsoft.com/c23436a7-6206-47fc-bd8e-4b8df31b26d9">MFP_GET_RATE_SET_EVENT</a>


</td>
</tr>
<tr>
<td>MFP_EVENT_TYPE_MEDIAITEM_CREATED</td>
<td>

<a href="https://msdn.microsoft.com/68e4076f-c03c-4780-9731-67eb6e78ec8b">MFP_MEDIAITEM_CREATED_EVENT</a>



<a href="https://msdn.microsoft.com/16187a19-6ea9-461a-a785-d302056c41ef">MFP_GET_MEDIAITEM_CREATED_EVENT</a>


</td>
</tr>
<tr>
<td>MFP_EVENT_TYPE_MEDIAITEM_SET</td>
<td>

<a href="https://msdn.microsoft.com/51ff492f-8199-4e1a-8d8b-d86bbb3c98dc">MFP_MEDIAITEM_SET_EVENT</a>



<a href="https://msdn.microsoft.com/3a03a657-0c93-496c-b3dc-6afeef7ee03f">MFP_GET_MEDIAITEM_SET_EVENT</a>


</td>
</tr>
<tr>
<td>MFP_EVENT_TYPE_FRAME_STEP</td>
<td>

<a href="https://msdn.microsoft.com/a395e94a-8d6d-48f5-9461-9f329af984c0">MFP_FRAME_STEP_EVENT</a>



<a href="https://msdn.microsoft.com/3ddb2d5e-d9ef-4bfd-892e-d59f430f818a">MFP_GET_FRAME_STEP_EVENT</a>


</td>
</tr>
<tr>
<td>MFP_EVENT_TYPE_MEDIAITEM_CLEARED</td>
<td>

<a href="https://msdn.microsoft.com/74218ab7-75a7-49e6-bfaa-5f57b1788a19">MFP_MEDIAITEM_CLEARED_EVENT</a>



<a href="https://msdn.microsoft.com/1e3c0882-2a8a-4fe9-9f05-5a343acea456">MFP_GET_MEDIAITEM_CLEARED_EVENT</a>


</td>
</tr>
<tr>
<td>MFP_EVENT_TYPE_MF</td>
<td>

<a href="https://msdn.microsoft.com/61dec86d-919c-4b1b-ab2a-527d062ae0f8">MFP_MF_EVENT</a>



<a href="https://msdn.microsoft.com/478cc749-1073-4fca-bfc6-3e5d5b0deec4">MFP_GET_MF_EVENT</a>


</td>
</tr>
<tr>
<td>MFP_EVENT_TYPE_ERROR</td>
<td>

<a href="https://msdn.microsoft.com/0ccfdefa-4913-4a02-bb91-14df1c185ddf">MFP_ERROR_EVENT</a>



<a href="https://msdn.microsoft.com/a8a86e1d-f009-4352-a388-822c2577ebe3">MFP_GET_ERROR_EVENT</a>


</td>
</tr>
<tr>
<td>MFP_EVENT_TYPE_PLAYBACK_ENDED</td>
<td>

<a href="https://msdn.microsoft.com/08cea881-dce9-4170-9b44-9943b014d300">MFP_PLAYBACK_ENDED_EVENT</a>



<a href="https://msdn.microsoft.com/c15a7473-41e5-4d84-aaaa-c547dd38826b">MFP_GET_PLAYBACK_ENDED_EVENT</a>


</td>
</tr>
<tr>
<td>MFP_EVENT_TYPE_ACQUIRE_USER_CREDENTIAL</td>
<td>

<a href="https://msdn.microsoft.com/61767b81-8641-43d5-b272-148d52517727">MFP_ACQUIRE_USER_CREDENTIAL_EVENT</a>



<a href="https://msdn.microsoft.com/4079acb8-8ae2-46e3-b7d9-50a700696fd6">MFP_GET_ACQUIRE_USER_CREDENTIAL_EVENT</a>


</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/7d9d01bf-861a-4c35-93b1-dbf85cbf0a32">IMFPMediaPlayerCallback</a>



<a href="https://msdn.microsoft.com/f26a730f-18c4-4247-acaf-af1dfad19086">Media Foundation Enumerations</a>
 

 

