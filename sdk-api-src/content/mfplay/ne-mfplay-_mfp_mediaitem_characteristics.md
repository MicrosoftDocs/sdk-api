---
UID: NE:mfplay._MFP_MEDIAITEM_CHARACTERISTICS
title: "_MFP_MEDIAITEM_CHARACTERISTICS"
author: windows-sdk-content
description: Contains flags that describe a media item.
old-location: mf\_mfp_mediaitem_characteristics.htm
tech.root: medfound
ms.assetid: 7bbb45e6-717d-413c-95fd-db730ab960ff
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: MFP_MEDIAITEM_CAN_PAUSE, MFP_MEDIAITEM_CAN_SEEK, MFP_MEDIAITEM_HAS_SLOW_SEEK, MFP_MEDIAITEM_IS_LIVE, _MFP_MEDIAITEM_CHARACTERISTICS, _MFP_MEDIAITEM_CHARACTERISTICS enumeration [Media Foundation], mf._mfp_mediaitem_characteristics, mfplay/MFP_MEDIAITEM_CAN_PAUSE, mfplay/MFP_MEDIAITEM_CAN_SEEK, mfplay/MFP_MEDIAITEM_HAS_SLOW_SEEK, mfplay/MFP_MEDIAITEM_IS_LIVE, mfplay/_MFP_MEDIAITEM_CHARACTERISTICS
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
 - _MFP_MEDIAITEM_CHARACTERISTICS
product: Windows
targetos: Windows
req.typenames: "_MFP_MEDIAITEM_CHARACTERISTICS"
req.redist: 
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
 

 

