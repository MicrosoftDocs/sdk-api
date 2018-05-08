---
UID: NF:strmif.IDvdControl.KaraokeAudioPresentationModeChange
title: IDvdControl::KaraokeAudioPresentationModeChange
author: windows-driver-content
description: Note  The IDvdControl interface is deprecated. Use IDvdControl2 instread. Sets the audio playback mode to karaoke.
old-location: dshow\idvdcontrol_karaokeaudiopresentationmodechange.htm
old-project: DirectShow
ms.assetid: a724af67-6aac-4307-97bc-a79e73621ce1
ms.author: windowsdriverdev
ms.date: 4/30/2018
ms.keywords: IDvdControl interface [DirectShow],KaraokeAudioPresentationModeChange method, IDvdControl.KaraokeAudioPresentationModeChange, IDvdControl::KaraokeAudioPresentationModeChange, IDvdControlKaraokeAudioPresentationModeChange, KaraokeAudioPresentationModeChange, KaraokeAudioPresentationModeChange method [DirectShow], KaraokeAudioPresentationModeChange method [DirectShow],IDvdControl interface, dshow.idvdcontrol_karaokeaudiopresentationmodechange, strmif/IDvdControl::KaraokeAudioPresentationModeChange
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
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
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmif.h
api_name:
-	IDvdControl.KaraokeAudioPresentationModeChange
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IDvdControl::KaraokeAudioPresentationModeChange


## -description



<div class="alert"><b>Note</b>  The <b>IDvdControl</b> interface is deprecated. Use <a href="https://msdn.microsoft.com/eda43b20-1c4d-4769-bb87-3942716af13c">IDvdControl2</a> instread.</div>
<div> </div>
Sets the audio playback mode to karaoke.




## -parameters




### -param ulMode [in]

Requested audio playback mode.


## -returns



Returns an <b>HRESULT</b> value.




## -remarks



Karaoke support is currently not implemented.

This method returns an error unless the domain is DVD_DOMAIN_VideoManagerMenu, DVD_DOMAIN_VideoTitleSetMenu, DVD_DOMAIN_Title, or DVD_DOMAIN_Stop. For more information, see <a href="https://msdn.microsoft.com/2763a159-d4de-44c2-905b-5828f328cbd2">DVD_DOMAIN</a>.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/a6ca0fe8-84e3-43e6-9421-29dcff056dfd">IDvdControl Interface</a>
 

 

