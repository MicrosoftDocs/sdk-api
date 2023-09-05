---
UID: NS:dvdmedia.AM_DVDCOPY_SET_COPY_STATE
title: AM_DVDCOPY_SET_COPY_STATE (dvdmedia.h)
description: Specifies the copy protection state of the filter.
helpviewer_keywords: ["*PAM_DVDCOPY_SET_COPY_STATE","AM_DVDCOPY_SET_COPY_STATE","AM_DVDCOPY_SET_COPY_STATE structure [DirectShow]","PAM_DVDCOPY_SET_COPY_STATE","PAM_DVDCOPY_SET_COPY_STATE structure pointer [DirectShow]","dshow.am_dvdcopy_set_copy_state","dvdmedia/AM_DVDCOPY_SET_COPY_STATE","dvdmedia/PAM_DVDCOPY_SET_COPY_STATE"]
old-location: dshow\am_dvdcopy_set_copy_state.htm
tech.root: dshow
ms.assetid: 0ad15402-096c-4967-bebc-10652535e502
ms.date: 4/26/2023
ms.keywords: '*PAM_DVDCOPY_SET_COPY_STATE, AM_DVDCOPY_SET_COPY_STATE, AM_DVDCOPY_SET_COPY_STATE structure [DirectShow], PAM_DVDCOPY_SET_COPY_STATE, PAM_DVDCOPY_SET_COPY_STATE structure pointer [DirectShow], dshow.am_dvdcopy_set_copy_state, dvdmedia/AM_DVDCOPY_SET_COPY_STATE, dvdmedia/PAM_DVDCOPY_SET_COPY_STATE'
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
req.typenames: AM_DVDCOPY_SET_COPY_STATE, *PAM_DVDCOPY_SET_COPY_STATE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - AM_DVDCOPY_SET_COPY_STATE
 - dvdmedia/AM_DVDCOPY_SET_COPY_STATE
 - PAM_DVDCOPY_SET_COPY_STATE
 - dvdmedia/PAM_DVDCOPY_SET_COPY_STATE
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
 - AM_DVDCOPY_SET_COPY_STATE
---

# AM_DVDCOPY_SET_COPY_STATE structure


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

Specifies the copy protection state of the filter.

## -struct-fields

### -field DVDCopyState

Copy protection state of the filter. Member of the <a href="/windows/desktop/api/dvdmedia/ne-dvdmedia-am_dvdcopystate">AM_DVDCOPYSTATE</a> enumerated data type.

## -remarks

Both the <a href="/windows/desktop/DirectShow/ikspropertyset-get">IKsPropertySet::Get</a> and <a href="/windows/desktop/DirectShow/ikspropertyset-set">IKsPropertySet::Set</a> methods are supported on this property. The Get method is called first to determine if authentication is required. If a filter provides multiple pins that use the same authenticator, such as a hardware DVD decoder, the decoder might respond with <b>AM_DVDCOPYSTATE_AUTHENTICATION_NOT_REQUIRED</b> on some pins to indicate that the key exchange algorithm only needs to be applied once. The filter should respond with <b>AM_DVDCOPYSTATE_AUTHENTICATION_REQUIRED</b> to get the copy protection state property on the first pin where this property is issued.

The Set method is used to indicate which phase of copy protection negotiation the filter is entering. Specify these by setting the required flag in the <a href="/windows/desktop/api/dvdmedia/ne-dvdmedia-am_dvdcopystate">AM_DVDCOPYSTATE</a> enumerated type.

The AM_PROPERTY_DVDCOPY_SET_COPY_STATE property uses this structure.

## -see-also

<a href="/windows/desktop/DirectShow/dvd-copy-protection-property-set">DVD Copy Protection Property Set</a>