---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# _MFP_MEDIAITEM_CHARACTERISTICS enumeration


## -description



<div class="alert"><b>Important</b>  Deprecated. This API may be removed from future releases of Windows. Applications should use the <a href="https://msdn.microsoft.com/dac99908-be90-415d-8837-2f97d573feb5">Media Session</a> for playback.</div>
<div> </div>


Contains flags that describe a media item.


## -enum-fields




### -field MFP_MEDIAITEM_IS_LIVE

The media item represents a live data source, such as video camera. If playback is stopped and then restarted, there will be a gap in the content.


### -field MFP_MEDIAITEM_CAN_SEEK

The media item supports seeking. If this flag is absent, the <a href="https://msdn.microsoft.com/d8665c3b-e0da-4a6f-a61b-38d507d1e78a">IMFPMediaPlayer::SetPosition</a> method will fail.


### -field MFP_MEDIAITEM_CAN_PAUSE

The media item can pause. If this flag is absent, the <a href="https://msdn.microsoft.com/f6bf6896-6ed6-4135-a01d-f875bfdc72f4">IMFPMediaPlayer::Pause</a> method will likely fail.


### -field MFP_MEDIAITEM_HAS_SLOW_SEEK

Seeking can take a long time. For example, the source might download content through HTTP.


## -remarks



The following <b>typedef</b> is defined for combining flags from this enumeration.

<pre class="syntax" xml:space="preserve"><code>typedef UINT32 MFP_MEDIAITEM_CHARACTERISTICS;</code></pre>



## -see-also




<a href="https://msdn.microsoft.com/9fe65644-c7a0-4af5-9765-f933215f5f83">IMFPMediaItem::GetCharacteristics</a>



<a href="https://msdn.microsoft.com/f26a730f-18c4-4247-acaf-af1dfad19086">Media Foundation Enumerations</a>
 

 

