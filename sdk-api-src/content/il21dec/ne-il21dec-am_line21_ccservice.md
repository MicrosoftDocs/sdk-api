---
UID: NE:il21dec._AM_LINE21_CCSERVICE
title: AM_LINE21_CCSERVICE (il21dec.h)
description: Indicates the closed captioning service.
helpviewer_keywords: ["*PAM_LINE21_CCSERVICE","AM_L21_CCSERVICE_Caption1","AM_L21_CCSERVICE_Caption2","AM_L21_CCSERVICE_None","AM_L21_CCSERVICE_Text1","AM_L21_CCSERVICE_Text2","AM_L21_CCSERVICE_XDS","AM_LINE21_CCSERVICE","AM_LINE21_CCSERVICE","AM_LINE21_CCSERVICE enumeration [DirectShow]","AM_LINE21_CCSERVICEEnumeration","PAM_LINE21_CCSERVICE","PAM_LINE21_CCSERVICE enumeration pointer [DirectShow]","dshow.am_line21_ccservice","il21dec/AM_L21_CCSERVICE_Caption1","il21dec/AM_L21_CCSERVICE_Caption2","il21dec/AM_L21_CCSERVICE_None","il21dec/AM_L21_CCSERVICE_Text1","il21dec/AM_L21_CCSERVICE_Text2","il21dec/AM_L21_CCSERVICE_XDS","il21dec/AM_LINE21_CCSERVICE","il21dec/PAM_LINE21_CCSERVICE"]
old-location: dshow\am_line21_ccservice.htm
tech.root: dshow
ms.assetid: dd2b618f-ffbf-4d48-bbe8-6d237a0f54e8
ms.date: 4/26/2023
ms.keywords: '*PAM_LINE21_CCSERVICE, AM_L21_CCSERVICE_Caption1, AM_L21_CCSERVICE_Caption2, AM_L21_CCSERVICE_None, AM_L21_CCSERVICE_Text1, AM_L21_CCSERVICE_Text2, AM_L21_CCSERVICE_XDS, AM_LINE21_CCSERVICE, AM_LINE21_CCSERVICE , AM_LINE21_CCSERVICE enumeration [DirectShow], AM_LINE21_CCSERVICEEnumeration, PAM_LINE21_CCSERVICE, PAM_LINE21_CCSERVICE enumeration pointer [DirectShow], dshow.am_line21_ccservice, il21dec/AM_L21_CCSERVICE_Caption1, il21dec/AM_L21_CCSERVICE_Caption2, il21dec/AM_L21_CCSERVICE_None, il21dec/AM_L21_CCSERVICE_Text1, il21dec/AM_L21_CCSERVICE_Text2, il21dec/AM_L21_CCSERVICE_XDS, il21dec/AM_LINE21_CCSERVICE, il21dec/PAM_LINE21_CCSERVICE'
req.header: il21dec.h
req.include-header: 
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
req.typenames: AM_LINE21_CCSERVICE, *PAM_LINE21_CCSERVICE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _AM_LINE21_CCSERVICE
 - il21dec/_AM_LINE21_CCSERVICE
 - PAM_LINE21_CCSERVICE
 - il21dec/PAM_LINE21_CCSERVICE
 - AM_LINE21_CCSERVICE
 - il21dec/AM_LINE21_CCSERVICE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - il21dec.h
api_name:
 - AM_LINE21_CCSERVICE
---

# AM_LINE21_CCSERVICE enumeration


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

Indicates the closed captioning service.

## -enum-fields

### -field AM_L21_CCSERVICE_None:0

No current service.

### -field AM_L21_CCSERVICE_Caption1

CC1 (caption channel).

### -field AM_L21_CCSERVICE_Caption2

CC2 (caption channel).

### -field AM_L21_CCSERVICE_Text1

T1 (text channel).

### -field AM_L21_CCSERVICE_Text2

T2 (text channel)

### -field AM_L21_CCSERVICE_XDS

Extended Data Services (XDS or EDS).

### -field AM_L21_CCSERVICE_DefChannel:10

### -field AM_L21_CCSERVICE_Invalid

## -remarks

The Line 21 decoder supports CC1 and CC2 only.

## -see-also

<a href="/windows/desktop/DirectShow/directshow-enumerated-types">DirectShow Enumerated Types</a>



<a href="/windows/desktop/api/il21dec/nf-il21dec-iamline21decoder-getcurrentservice">IAMLine21Decoder::GetCurrentService</a>



<a href="/windows/desktop/api/il21dec/nf-il21dec-iamline21decoder-setcurrentservice">IAMLine21Decoder::SetCurrentService</a>
