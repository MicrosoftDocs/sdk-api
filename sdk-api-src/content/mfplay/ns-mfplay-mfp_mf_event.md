---
UID: NS:mfplay.MFP_MF_EVENT
title: MFP_MF_EVENT
author: windows-driver-content
description: Event structure for the MFP_EVENT_TYPE_MF event.
old-location: mf\mfp_mf_event.htm
old-project: medfound
ms.assetid: 61dec86d-919c-4b1b-ab2a-527d062ae0f8
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: MFP_MF_EVENT, MFP_MF_EVENT structure [Media Foundation], mf.mfp_mf_event, mfplay/MFP_MF_EVENT
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: MFP_MF_EVENT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	mfplay.h
api_name:
-	MFP_MF_EVENT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# MFP_MF_EVENT structure


## -description



<div class="alert"><b>Important</b>  Deprecated. This API may be removed from future releases of Windows. Applications should use the <a href="https://msdn.microsoft.com/dac99908-be90-415d-8837-2f97d573feb5">Media Session</a> for playback.</div>
<div> </div>


Event structure for the <b>MFP_EVENT_TYPE_MF</b> event. The MFPlay player object uses this event to forward certain events from the Media Foundation pipeline to the application.


## -struct-fields




### -field header


<a href="https://msdn.microsoft.com/ed9d3790-845a-4392-b755-6a5ce6e20de5">MFP_EVENT_HEADER</a> structure that contains data common to all <a href="https://msdn.microsoft.com/fa57d465-1ee9-4f7a-9be8-66a6d73f65e8">IMFPMediaPlayer</a> events.


### -field MFEventType

Media Foundation event type. Currently, the MFPlay player object forwards the following pipeline events to the application:

<table>
<tr>
<th>Event</th>
<th>Description</th>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/8637dfcd-2e0c-4cf4-a216-4089c201bfc6">MEBufferingStarted</a>
</td>
<td>The source has started buffering data.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/11b1290d-d462-4aa0-a358-b3f6447c99d8">MEBufferingStopped</a>
</td>
<td>The source has stopped buffering data.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/a54a446c-0e96-467b-90f6-0f64a7c1727d">MEExtendedType</a>
</td>
<td>Custom event type.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/228e069a-a26b-472e-915e-ff9aec5ee9c1">MEReconnectEnd</a>
</td>
<td>The source has completed an attempt to reconnect to the server.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/c5975279-c710-4046-9152-d1e1c62eb785">MEReconnectStart</a>
</td>
<td>The source is attempting to reconnect to the server.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/bb7db7c9-c39f-4bf4-9412-42525c4f2ea3">MERendererEvent</a>
</td>
<td>Event sent by a renderer, such as the <a href="https://msdn.microsoft.com/1c985558-d25d-4f51-978a-58c05943dab9">Enhanced Video Renderer</a> (EVR).</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/9eeb4262-1593-4c5f-9341-ebd328b586e7">MEStreamSinkFormatChanged</a>
</td>
<td>A stream format has changed.</td>
</tr>
</table>
 


### -field pMFMediaEvent

Pointer to the <a href="https://msdn.microsoft.com/b4f686be-9472-433c-b983-6c48dfd3ac76">IMFMediaEvent</a> interface of the Media Foundation event.


### -field pMediaItem

Pointer to the <a href="https://msdn.microsoft.com/2839d256-bdaf-40cf-9f9d-46f9e2ce59e8">IMFPMediaItem</a> interface of the current media item.


## -remarks




        To get a pointer to this structure, cast the <i>pEventHeader</i> parameter of the <a href="https://msdn.microsoft.com/2a80a9d0-83ee-4bb0-ab2c-0f68367f3bf8">IMFPMediaPlayerCallback::OnMediaPlayerEvent</a> method. You can use the <a href="https://msdn.microsoft.com/478cc749-1073-4fca-bfc6-3e5d5b0deec4">MFP_GET_MF_EVENT</a> macro for this purpose.

If <b>MFEventType</b> is <a href="https://msdn.microsoft.com/9eeb4262-1593-4c5f-9341-ebd328b586e7">MEStreamSinkFormatChanged</a>, the following property may be stored in the event property store, which can be accessed through the <b>header.pPropertyStore</b> member.

<table>
<tr>
<th>Property</th>
<th>Description</th>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/086fcb1e-f75a-4f38-9fe1-77d30f64bc89">MFP_PKEY_StreamIndex</a>
</td>
<td>The index of the stream whose format changed. </td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/7d9d01bf-861a-4c35-93b1-dbf85cbf0a32">IMFPMediaPlayerCallback</a>



<a href="https://msdn.microsoft.com/39fdd724-13ca-48ab-8a55-93529d1da3b4">Media Foundation Structures</a>



<a href="https://msdn.microsoft.com/6f143c51-ec46-46d4-9a1e-b04fcc0d8bea">Using MFPlay for Audio/Video Playback</a>
 

 

