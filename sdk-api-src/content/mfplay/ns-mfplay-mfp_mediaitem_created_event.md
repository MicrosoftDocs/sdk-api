---
UID: NS:mfplay.MFP_MEDIAITEM_CREATED_EVENT
title: MFP_MEDIAITEM_CREATED_EVENT
author: windows-driver-content
description: Event structure for the MFP_EVENT_TYPE_MEDIAITEM_CREATED event.
old-location: mf\mfp_mediaitem_created_event.htm
old-project: medfound
ms.assetid: 68e4076f-c03c-4780-9731-67eb6e78ec8b
ms.author: windowsdriverdev
ms.date: 4/23/2018
ms.keywords: MFP_MEDIAITEM_CREATED_EVENT, MFP_MEDIAITEM_CREATED_EVENT structure [Media Foundation], mf.mfp_mediaitem_created_event, mfplay/MFP_MEDIAITEM_CREATED_EVENT
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
req.typenames: MFP_MEDIAITEM_CREATED_EVENT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	mfplay.h
api_name:
-	MFP_MEDIAITEM_CREATED_EVENT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# MFP_MEDIAITEM_CREATED_EVENT structure


## -description



<div class="alert"><b>Important</b>  Deprecated. This API may be removed from future releases of Windows. Applications should use the <a href="https://msdn.microsoft.com/dac99908-be90-415d-8837-2f97d573feb5">Media Session</a> for playback.</div>
<div> </div>


Event structure for the <b>MFP_EVENT_TYPE_MEDIAITEM_CREATED</b> event. This event is sent when the <a href="https://msdn.microsoft.com/7dc2a7f3-81b4-46c6-b45e-44c6a20afc6b">IMFPMediaPlayer::CreateMediaItemFromURL</a> or  <a href="https://msdn.microsoft.com/d647df89-b874-448e-ae41-ee3bcb55521f">IMFPMediaPlayer::CreateMediaItemFromObject</a> method completes.


## -struct-fields




### -field header


<a href="https://msdn.microsoft.com/ed9d3790-845a-4392-b755-6a5ce6e20de5">MFP_EVENT_HEADER</a> structure that contains data common to all <a href="https://msdn.microsoft.com/fa57d465-1ee9-4f7a-9be8-66a6d73f65e8">IMFPMediaPlayer</a> events.


### -field pMediaItem

Pointer to the <a href="https://msdn.microsoft.com/2839d256-bdaf-40cf-9f9d-46f9e2ce59e8">IMFPMediaItem</a> interface of the new media item. If creating the media item failed, this member is <b>NULL</b>.


### -field dwUserData

Application-defined user data for the media item. This value is specified when the application calls <a href="https://msdn.microsoft.com/7dc2a7f3-81b4-46c6-b45e-44c6a20afc6b">CreateMediaItemFromURL</a> or  <a href="https://msdn.microsoft.com/d647df89-b874-448e-ae41-ee3bcb55521f">CreateMediaItemFromObject</a>.


## -remarks



To get a pointer to this structure, cast the <i>pEventHeader</i>
parameter of the <a href="https://msdn.microsoft.com/2a80a9d0-83ee-4bb0-ab2c-0f68367f3bf8">IMFPMediaPlayerCallback::OnMediaPlayerEvent</a>  method.  You can use the <a href="https://msdn.microsoft.com/16187a19-6ea9-461a-a785-d302056c41ef">MFP_GET_MEDIAITEM_CREATED_EVENT</a> macro for this purpose.

Media items are created asynchronously. If multiple items are created, the operations can complete in any order, not necessarily in the same order as the method calls. You can use  the <b>dwUserData</b> member to identify the items, if you have simultaneous requests pending. 




## -see-also




<a href="https://msdn.microsoft.com/7d9d01bf-861a-4c35-93b1-dbf85cbf0a32">IMFPMediaPlayerCallback</a>



<a href="https://msdn.microsoft.com/39fdd724-13ca-48ab-8a55-93529d1da3b4">Media Foundation Structures</a>



<a href="https://msdn.microsoft.com/6f143c51-ec46-46d4-9a1e-b04fcc0d8bea">Using MFPlay for Audio/Video Playback</a>
 

 

