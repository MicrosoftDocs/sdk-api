---
UID: NS:iwstdec._AM_WST_PAGE
title: AM_WST_PAGE (iwstdec.h)
description: The AM_WST_PAGE structure identifies a World Standard Teletext (WST) page.
helpviewer_keywords: ["*PAM_WST_PAGE","AM_WST_PAGE","AM_WST_PAGE structure [DirectShow]","AM_WST_PAGEStructure","PAM_WST_PAGE","PAM_WST_PAGE structure pointer [DirectShow]","dshow.am_wst_page","iwstdec/AM_WST_PAGE","iwstdec/PAM_WST_PAGE"]
old-location: dshow\am_wst_page.htm
tech.root: dshow
ms.assetid: 6bed254f-35e4-40d0-9a59-0a2575aa61e1
ms.date: 4/26/2023
ms.keywords: '*PAM_WST_PAGE, AM_WST_PAGE, AM_WST_PAGE structure [DirectShow], AM_WST_PAGEStructure, PAM_WST_PAGE, PAM_WST_PAGE structure pointer [DirectShow], dshow.am_wst_page, iwstdec/AM_WST_PAGE, iwstdec/PAM_WST_PAGE'
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
req.typenames: AM_WST_PAGE, *PAM_WST_PAGE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _AM_WST_PAGE
 - iwstdec/_AM_WST_PAGE
 - PAM_WST_PAGE
 - iwstdec/PAM_WST_PAGE
 - AM_WST_PAGE
 - iwstdec/AM_WST_PAGE
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
 - AM_WST_PAGE
---

# AM_WST_PAGE structure


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The AM_WST_PAGE structure identifies a World Standard Teletext (WST) page.

## -struct-fields

### -field dwPageNr

The page number.

### -field dwSubPageNr

The sub-page number.

### -field pucPageData

A pointer to the page data.

## -see-also

<a href="/windows/desktop/DirectShow/directshow-structures">DirectShow Structures</a>



<a href="/windows/desktop/api/iwstdec/nn-iwstdec-iamwstdecoder">IAMWstDecoder</a>