---
UID: NF:strmif.IDvdControl.KaraokeAudioPresentationModeChange
title: IDvdControl::KaraokeAudioPresentationModeChange (strmif.h)
description: Note  The IDvdControl interface is deprecated. Use IDvdControl2 instread. Sets the audio playback mode to karaoke.
helpviewer_keywords: ["IDvdControl interface [DirectShow]","KaraokeAudioPresentationModeChange method","IDvdControl.KaraokeAudioPresentationModeChange","IDvdControl::KaraokeAudioPresentationModeChange","IDvdControlKaraokeAudioPresentationModeChange","KaraokeAudioPresentationModeChange","KaraokeAudioPresentationModeChange method [DirectShow]","KaraokeAudioPresentationModeChange method [DirectShow]","IDvdControl interface","dshow.idvdcontrol_karaokeaudiopresentationmodechange","strmif/IDvdControl::KaraokeAudioPresentationModeChange"]
old-location: dshow\idvdcontrol_karaokeaudiopresentationmodechange.htm
tech.root: dshow
ms.assetid: a724af67-6aac-4307-97bc-a79e73621ce1
ms.date: 12/05/2018
ms.keywords: IDvdControl interface [DirectShow],KaraokeAudioPresentationModeChange method, IDvdControl.KaraokeAudioPresentationModeChange, IDvdControl::KaraokeAudioPresentationModeChange, IDvdControlKaraokeAudioPresentationModeChange, KaraokeAudioPresentationModeChange, KaraokeAudioPresentationModeChange method [DirectShow], KaraokeAudioPresentationModeChange method [DirectShow],IDvdControl interface, dshow.idvdcontrol_karaokeaudiopresentationmodechange, strmif/IDvdControl::KaraokeAudioPresentationModeChange
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDvdControl::KaraokeAudioPresentationModeChange
 - strmif/IDvdControl::KaraokeAudioPresentationModeChange
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmif.h
api_name:
 - IDvdControl.KaraokeAudioPresentationModeChange
---

# IDvdControl::KaraokeAudioPresentationModeChange


## -description

<div class="alert"><b>Note</b>  The <b>IDvdControl</b> interface is deprecated. Use <a href="/windows/desktop/api/strmif/nn-strmif-idvdcontrol2">IDvdControl2</a> instread.</div>
<div> </div>
Sets the audio playback mode to karaoke.

## -parameters

### -param ulMode [in]

Requested audio playback mode.

## -returns

Returns an <b>HRESULT</b> value.

## -remarks

Karaoke support is currently not implemented.

This method returns an error unless the domain is DVD_DOMAIN_VideoManagerMenu, DVD_DOMAIN_VideoTitleSetMenu, DVD_DOMAIN_Title, or DVD_DOMAIN_Stop. For more information, see <a href="/windows/desktop/api/strmif/ne-strmif-dvd_domain">DVD_DOMAIN</a>.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-idvdcontrol">IDvdControl Interface</a>