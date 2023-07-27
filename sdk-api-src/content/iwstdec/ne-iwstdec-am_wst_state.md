---
UID: NE:iwstdec._AM_WST_STATE
title: AM_WST_STATE (iwstdec.h)
description: The AM_WST_STATE enumeration specifies whether WST closed captioning is enabled or disabled.
helpviewer_keywords: ["*PAM_WST_STATE","AM_WST_STATE","AM_WST_STATE","AM_WST_STATE enumeration [DirectShow]","AM_WST_STATEEnumeration","AM_WST_STATE_Off","AM_WST_STATE_On","PAM_WST_STATE","PAM_WST_STATE enumeration pointer [DirectShow]","dshow.am_wst_state","iwstdec/AM_WST_STATE","iwstdec/AM_WST_STATE_Off","iwstdec/AM_WST_STATE_On","iwstdec/PAM_WST_STATE"]
old-location: dshow\am_wst_state.htm
tech.root: dshow
ms.assetid: b6548144-7e18-4d5d-9243-51eb7db9821b
ms.date: 4/26/2023
ms.keywords: '*PAM_WST_STATE, AM_WST_STATE, AM_WST_STATE , AM_WST_STATE enumeration [DirectShow], AM_WST_STATEEnumeration, AM_WST_STATE_Off, AM_WST_STATE_On, PAM_WST_STATE, PAM_WST_STATE enumeration pointer [DirectShow], dshow.am_wst_state, iwstdec/AM_WST_STATE, iwstdec/AM_WST_STATE_Off, iwstdec/AM_WST_STATE_On, iwstdec/PAM_WST_STATE'
req.header: iwstdec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: AM_WST_STATE, *PAM_WST_STATE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _AM_WST_STATE
 - iwstdec/_AM_WST_STATE
 - PAM_WST_STATE
 - iwstdec/PAM_WST_STATE
 - AM_WST_STATE
 - iwstdec/AM_WST_STATE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - iwstdec.h
api_name:
 - AM_WST_STATE
---

# AM_WST_STATE enumeration


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>AM_WST_STATE</b> enumeration specifies whether WST closed captioning is enabled or disabled.

## -enum-fields

### -field AM_WST_STATE_Off:0

Specifies that WST closed captioning is enabled.

### -field AM_WST_STATE_On

Specifies that WST closed captioning is disabled.

## -see-also

<a href="/windows/desktop/DirectShow/directshow-enumerated-types">DirectShow Enumerated Types</a>



<a href="/windows/desktop/api/iwstdec/nn-iwstdec-iamwstdecoder">IAMWstDecoder</a>
