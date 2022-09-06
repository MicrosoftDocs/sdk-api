---
UID: NE:mfplay._MFP_MEDIAITEM_CHARACTERISTICS
title: _MFP_MEDIAITEM_CHARACTERISTICS (mfplay.h)
description: Contains flags that describe a media item.
helpviewer_keywords: ["MFP_MEDIAITEM_CAN_PAUSE","MFP_MEDIAITEM_CAN_SEEK","MFP_MEDIAITEM_HAS_SLOW_SEEK","MFP_MEDIAITEM_IS_LIVE","_MFP_MEDIAITEM_CHARACTERISTICS","_MFP_MEDIAITEM_CHARACTERISTICS enumeration [Media Foundation]","mf._mfp_mediaitem_characteristics","mfplay/MFP_MEDIAITEM_CAN_PAUSE","mfplay/MFP_MEDIAITEM_CAN_SEEK","mfplay/MFP_MEDIAITEM_HAS_SLOW_SEEK","mfplay/MFP_MEDIAITEM_IS_LIVE","mfplay/_MFP_MEDIAITEM_CHARACTERISTICS"]
old-location: mf\_mfp_mediaitem_characteristics.htm
tech.root: mf
ms.assetid: 7bbb45e6-717d-413c-95fd-db730ab960ff
ms.date: 12/05/2018
ms.keywords: MFP_MEDIAITEM_CAN_PAUSE, MFP_MEDIAITEM_CAN_SEEK, MFP_MEDIAITEM_HAS_SLOW_SEEK, MFP_MEDIAITEM_IS_LIVE, _MFP_MEDIAITEM_CHARACTERISTICS, _MFP_MEDIAITEM_CHARACTERISTICS enumeration [Media Foundation], mf._mfp_mediaitem_characteristics, mfplay/MFP_MEDIAITEM_CAN_PAUSE, mfplay/MFP_MEDIAITEM_CAN_SEEK, mfplay/MFP_MEDIAITEM_HAS_SLOW_SEEK, mfplay/MFP_MEDIAITEM_IS_LIVE, mfplay/_MFP_MEDIAITEM_CHARACTERISTICS
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
targetos: Windows
req.typenames: _MFP_MEDIAITEM_CHARACTERISTICS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MFP_MEDIAITEM_CHARACTERISTICS
 - mfplay/_MFP_MEDIAITEM_CHARACTERISTICS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mfplay.h
api_name:
 - _MFP_MEDIAITEM_CHARACTERISTICS
---

# _MFP_MEDIAITEM_CHARACTERISTICS enumeration


## -description

<div class="alert"><b>Important</b>  Deprecated. This API may be removed from future releases of Windows. Applications should use the <a href="/windows/desktop/medfound/media-session">Media Session</a> for playback.</div>
<div> </div>


Contains flags that describe a media item.

## -enum-fields

### -field MFP_MEDIAITEM_IS_LIVE:0x1

The media item represents a live data source, such as video camera. If playback is stopped and then restarted, there will be a gap in the content.

### -field MFP_MEDIAITEM_CAN_SEEK:0x2

The media item supports seeking. If this flag is absent, the <a href="/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setposition">IMFPMediaPlayer::SetPosition</a> method will fail.

### -field MFP_MEDIAITEM_CAN_PAUSE:0x4

The media item can pause. If this flag is absent, the <a href="/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-pause">IMFPMediaPlayer::Pause</a> method will likely fail.

### -field MFP_MEDIAITEM_HAS_SLOW_SEEK:0x8

Seeking can take a long time. For example, the source might download content through HTTP.

## -remarks

The following <b>typedef</b> is defined for combining flags from this enumeration.


``` syntax
typedef UINT32 MFP_MEDIAITEM_CHARACTERISTICS;
```


## -see-also

<a href="/windows/desktop/api/mfplay/nf-mfplay-imfpmediaitem-getcharacteristics">IMFPMediaItem::GetCharacteristics</a>



<a href="/windows/desktop/medfound/media-foundation-enumerations">Media Foundation Enumerations</a>
