---
UID: NS:dvdmedia._AM_DVDCOPY_BUSKEY
title: AM_DVDCOPY_BUSKEY (dvdmedia.h)
description: Identifies the DVD bus key.
helpviewer_keywords: ["*PAM_DVDCOPY_BUSKEY","AM_DVDCOPY_BUSKEY","AM_DVDCOPY_BUSKEY structure [DirectShow]","PAM_DVDCOPY_BUSKEY","PAM_DVDCOPY_BUSKEY structure pointer [DirectShow]","dshow.am_dvdcopy_buskey","dvdmedia/AM_DVDCOPY_BUSKEY","dvdmedia/PAM_DVDCOPY_BUSKEY"]
old-location: dshow\am_dvdcopy_buskey.htm
tech.root: dshow
ms.assetid: 9f55dcc1-cb59-40ce-82d0-7f2066cb9d03
ms.date: 4/26/2023
ms.keywords: '*PAM_DVDCOPY_BUSKEY, AM_DVDCOPY_BUSKEY, AM_DVDCOPY_BUSKEY structure [DirectShow], PAM_DVDCOPY_BUSKEY, PAM_DVDCOPY_BUSKEY structure pointer [DirectShow], dshow.am_dvdcopy_buskey, dvdmedia/AM_DVDCOPY_BUSKEY, dvdmedia/PAM_DVDCOPY_BUSKEY'
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
req.typenames: AM_DVDCOPY_BUSKEY, *PAM_DVDCOPY_BUSKEY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _AM_DVDCOPY_BUSKEY
 - dvdmedia/_AM_DVDCOPY_BUSKEY
 - PAM_DVDCOPY_BUSKEY
 - dvdmedia/PAM_DVDCOPY_BUSKEY
 - AM_DVDCOPY_BUSKEY
 - dvdmedia/AM_DVDCOPY_BUSKEY
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
 - AM_DVDCOPY_BUSKEY
---

# AM_DVDCOPY_BUSKEY structure


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

Identifies the DVD bus key.

## -struct-fields

### -field BusKey

DVD drive bus key.

### -field Reserved

Reserved.

## -remarks

The AM_PROPERTY_DVDCOPY_DVD_KEY1 and AM_PROPERTY_DVDCOPY_DEC_KEY2 properties use this structure.

A bus key is used for the DVD CSS key exchange for decryption. Implementors should get a CSS license and further instructions from CSS.

## -see-also

<a href="/windows/desktop/DirectShow/dvd-copy-protection-property-set">DVD Copy Protection Property Set</a>