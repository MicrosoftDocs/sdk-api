---
UID: NE:dvdmedia.AM_DVDCOPYSTATE
title: AM_DVDCOPYSTATE (dvdmedia.h)
description: Specifies the copy protection state.
helpviewer_keywords: ["AM_DVDCOPYSTATE","AM_DVDCOPYSTATE enumeration [DirectShow]","AM_DVDCOPYSTATE_AUTHENTICATION_NOT_REQUIRED","AM_DVDCOPYSTATE_AUTHENTICATION_REQUIRED","AM_DVDCOPYSTATE_DONE","AM_DVDCOPYSTATE_INITIALIZE","AM_DVDCOPYSTATE_INITIALIZE_TITLE","dshow.am_dvdcopystate","dvdmedia/AM_DVDCOPYSTATE","dvdmedia/AM_DVDCOPYSTATE_AUTHENTICATION_NOT_REQUIRED","dvdmedia/AM_DVDCOPYSTATE_AUTHENTICATION_REQUIRED","dvdmedia/AM_DVDCOPYSTATE_DONE","dvdmedia/AM_DVDCOPYSTATE_INITIALIZE","dvdmedia/AM_DVDCOPYSTATE_INITIALIZE_TITLE"]
old-location: dshow\am_dvdcopystate.htm
tech.root: dshow
ms.assetid: 32a9783e-f9f1-4e37-8cd2-3ff5634d75f6
ms.date: 4/26/2023
ms.keywords: AM_DVDCOPYSTATE, AM_DVDCOPYSTATE enumeration [DirectShow], AM_DVDCOPYSTATE_AUTHENTICATION_NOT_REQUIRED, AM_DVDCOPYSTATE_AUTHENTICATION_REQUIRED, AM_DVDCOPYSTATE_DONE, AM_DVDCOPYSTATE_INITIALIZE, AM_DVDCOPYSTATE_INITIALIZE_TITLE, dshow.am_dvdcopystate, dvdmedia/AM_DVDCOPYSTATE, dvdmedia/AM_DVDCOPYSTATE_AUTHENTICATION_NOT_REQUIRED, dvdmedia/AM_DVDCOPYSTATE_AUTHENTICATION_REQUIRED, dvdmedia/AM_DVDCOPYSTATE_DONE, dvdmedia/AM_DVDCOPYSTATE_INITIALIZE, dvdmedia/AM_DVDCOPYSTATE_INITIALIZE_TITLE
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
req.typenames: AM_DVDCOPYSTATE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - AM_DVDCOPYSTATE
 - dvdmedia/AM_DVDCOPYSTATE
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
 - AM_DVDCOPYSTATE
---

# AM_DVDCOPYSTATE enumeration


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

Specifies the copy protection state.

## -enum-fields

### -field AM_DVDCOPYSTATE_INITIALIZE:0

Starting a full key-exchange algorithm.

### -field AM_DVDCOPYSTATE_INITIALIZE_TITLE:1

Starting a title key-exchange algorithm.

### -field AM_DVDCOPYSTATE_AUTHENTICATION_NOT_REQUIRED:2

Authentication is not required.

### -field AM_DVDCOPYSTATE_AUTHENTICATION_REQUIRED:3

Authentication required.

### -field AM_DVDCOPYSTATE_DONE:4

Key exchange negotiation is complete.

## -remarks

The <a href="/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_set_copy_state">AM_DVDCOPY_SET_COPY_STATE</a> structure uses this data type.

## -see-also

<a href="/windows/desktop/DirectShow/dvd-copy-protection-property-set">DVD Copy Protection Property Set</a>

