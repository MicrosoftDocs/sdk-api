---
UID: NS:dvdmedia._AM_DVDCOPY_DISCKEY
title: AM_DVDCOPY_DISCKEY (dvdmedia.h)
description: Specifies the DVD disc key.
helpviewer_keywords: ["*PAM_DVDCOPY_DISCKEY","AM_DVDCOPY_DISCKEY","AM_DVDCOPY_DISCKEY structure [DirectShow]","PAM_DVDCOPY_DISCKEY","PAM_DVDCOPY_DISCKEY structure pointer [DirectShow]","dshow.am_dvdcopy_disckey","dvdmedia/AM_DVDCOPY_DISCKEY","dvdmedia/PAM_DVDCOPY_DISCKEY"]
old-location: dshow\am_dvdcopy_disckey.htm
tech.root: dshow
ms.assetid: ab4d7b2d-59a6-4ad1-9120-552747b96596
ms.date: 4/26/2023
ms.keywords: '*PAM_DVDCOPY_DISCKEY, AM_DVDCOPY_DISCKEY, AM_DVDCOPY_DISCKEY structure [DirectShow], PAM_DVDCOPY_DISCKEY, PAM_DVDCOPY_DISCKEY structure pointer [DirectShow], dshow.am_dvdcopy_disckey, dvdmedia/AM_DVDCOPY_DISCKEY, dvdmedia/PAM_DVDCOPY_DISCKEY'
req.header: dvdmedia.h
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
req.typenames: AM_DVDCOPY_DISCKEY, *PAM_DVDCOPY_DISCKEY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _AM_DVDCOPY_DISCKEY
 - dvdmedia/_AM_DVDCOPY_DISCKEY
 - PAM_DVDCOPY_DISCKEY
 - dvdmedia/PAM_DVDCOPY_DISCKEY
 - AM_DVDCOPY_DISCKEY
 - dvdmedia/AM_DVDCOPY_DISCKEY
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Dvdmedia.h
api_name:
 - AM_DVDCOPY_DISCKEY
---

# AM_DVDCOPY_DISCKEY structure


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

Specifies the DVD disc key.

## -struct-fields

### -field DiscKey

DVD disc key.

## -remarks

The AM_PROPERTY_DVDCOPY_DISC_KEY property uses this structure.

A disc key is used for the DVD CSS key exchange for decryption. Implementors should get a CSS license and further instructions from CSS.

## -see-also

<a href="/windows/desktop/DirectShow/dvd-copy-protection-property-set">DVD Copy Protection Property Set</a>