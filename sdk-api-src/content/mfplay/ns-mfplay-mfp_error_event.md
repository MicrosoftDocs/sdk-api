---
UID: NS:mfplay.MFP_ERROR_EVENT
title: MFP_ERROR_EVENT
author: windows-driver-content
description: Event structure for the MFP_EVENT_TYPE_ERROR event.
old-location: mf\mfp_error_event.htm
old-project: medfound
ms.assetid: 0ccfdefa-4913-4a02-bb91-14df1c185ddf
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: MFP_ERROR_EVENT, MFP_ERROR_EVENT structure [Media Foundation], mf.mfp_error_event, mfplay/MFP_ERROR_EVENT
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
req.typenames: MFP_ERROR_EVENT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	mfplay.h
api_name:
-	MFP_ERROR_EVENT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# MFP_ERROR_EVENT structure


## -description



<div class="alert"><b>Important</b>  Deprecated. This API may be removed from future releases of Windows. Applications should use the <a href="https://msdn.microsoft.com/dac99908-be90-415d-8837-2f97d573feb5">Media Session</a> for playback.</div>
<div> </div>


Event structure for the <b>MFP_EVENT_TYPE_ERROR</b> event. This event is sent if an error occurs during playback.  


## -struct-fields




### -field header


<a href="https://msdn.microsoft.com/ed9d3790-845a-4392-b755-6a5ce6e20de5">MFP_EVENT_HEADER</a> structure that contains data common to all <a href="https://msdn.microsoft.com/fa57d465-1ee9-4f7a-9be8-66a6d73f65e8">IMFPMediaPlayer</a> events. The <b>hrEvent</b> member of the structure contains the error code. 


## -remarks



To get a pointer to this structure, cast the <i>pEventHeader</i>
parameter of the <a href="https://msdn.microsoft.com/2a80a9d0-83ee-4bb0-ab2c-0f68367f3bf8">IMFPMediaPlayerCallback::OnMediaPlayerEvent</a>  method.  You can use the <a href="https://msdn.microsoft.com/a8a86e1d-f009-4352-a388-822c2577ebe3">MFP_GET_ERROR_EVENT</a> macro for this purpose.

This event is not used to signal the failure of an asynchronous <a href="https://msdn.microsoft.com/fa57d465-1ee9-4f7a-9be8-66a6d73f65e8">IMFPMediaPlayer</a> method. If an asynchronous method fails, the error is reported in the standard event listed for that method. The <b>MFP_EVENT_TYPE_ERROR</b> event is used for errors that happen outside the context of an asynchronous method call.




## -see-also




<a href="https://msdn.microsoft.com/7d9d01bf-861a-4c35-93b1-dbf85cbf0a32">IMFPMediaPlayerCallback</a>



<a href="https://msdn.microsoft.com/39fdd724-13ca-48ab-8a55-93529d1da3b4">Media Foundation Structures</a>



<a href="https://msdn.microsoft.com/6f143c51-ec46-46d4-9a1e-b04fcc0d8bea">Using MFPlay for Audio/Video Playback</a>
 

 

