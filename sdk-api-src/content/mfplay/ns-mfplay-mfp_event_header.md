---
UID: NS:mfplay.MFP_EVENT_HEADER
title: MFP_EVENT_HEADER
author: windows-sdk-content
description: Contains information that is common to every type of MFPlay event.
old-location: mf\mfp_event_header.htm
tech.root: medfound
ms.assetid: ed9d3790-845a-4392-b755-6a5ce6e20de5
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: MFP_EVENT_HEADER, MFP_EVENT_HEADER structure [Media Foundation], mf.mfp_event_header, mfplay/MFP_EVENT_HEADER
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
 - MFP_EVENT_HEADER
product: Windows
targetos: Windows
req.typenames: MFP_EVENT_HEADER
req.redist: 
---

# MFP_EVENT_HEADER structure


## -description



<div class="alert"><b>Important</b>  Deprecated. This API may be removed from future releases of Windows. Applications should use the <a href="https://msdn.microsoft.com/dac99908-be90-415d-8837-2f97d573feb5">Media Session</a> for playback.</div>
<div> </div>


Contains information that is common to  every type of MFPlay event.


## -struct-fields




### -field eEventType

The type of event, specified as a member of the <a href="https://msdn.microsoft.com/95beb13d-db84-4713-9c27-27b37eac7f2f">MFP_EVENT_TYPE</a> enumeration.


### -field hrEvent

Error or success code for the operation that caused the event.


### -field pMediaPlayer

Pointer to the <a href="https://msdn.microsoft.com/fa57d465-1ee9-4f7a-9be8-66a6d73f65e8">IMFPMediaPlayer</a> interface of the MFPlay player object that sent the event.


### -field eState

The new state of the MFPlay player object, specified as a member of the <a href="https://msdn.microsoft.com/a0d5c840-a1aa-48cf-bf2e-7e5c35951fb6">MFP_MEDIAPLAYER_STATE</a> enumeration.


### -field pPropertyStore

A pointer to the <b>IPropertyStore</b> interface of  a property store object. The property store is used to hold additional event data for some event types. This member might be <b>NULL</b>.


## -see-also




<a href="https://msdn.microsoft.com/7d9d01bf-861a-4c35-93b1-dbf85cbf0a32">IMFPMediaPlayerCallback</a>



<a href="https://msdn.microsoft.com/39fdd724-13ca-48ab-8a55-93529d1da3b4">Media Foundation Structures</a>



<a href="https://msdn.microsoft.com/6f143c51-ec46-46d4-9a1e-b04fcc0d8bea">Using MFPlay for Audio/Video Playback</a>
 

 

