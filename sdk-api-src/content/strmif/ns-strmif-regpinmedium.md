---
UID: NS:strmif.REGPINMEDIUM
title: REGPINMEDIUM (strmif.h)
description: The REGPINMEDIUM structure describes a pin medium for registration through the IFilterMapper2 interface.
helpviewer_keywords: ["REGPINMEDIUM","REGPINMEDIUM structure [DirectShow]","REGPINMEDIUMStructure","dshow.regpinmedium","strmif/REGPINMEDIUM"]
old-location: dshow\regpinmedium.htm
tech.root: dshow
ms.assetid: ed5614fe-bfeb-4ddf-a626-b14080f45b33
ms.date: 4/26/2023
ms.keywords: REGPINMEDIUM, REGPINMEDIUM structure [DirectShow], REGPINMEDIUMStructure, dshow.regpinmedium, strmif/REGPINMEDIUM
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
req.typenames: REGPINMEDIUM
req.redist: 
ms.custom: 19H1
f1_keywords:
 - REGPINMEDIUM
 - strmif/REGPINMEDIUM
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - strmif.h
api_name:
 - REGPINMEDIUM
---

# REGPINMEDIUM structure


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>REGPINMEDIUM</code> structure describes a pin medium for registration through the <a href="/windows/desktop/api/strmif/nn-strmif-ifiltermapper2">IFilterMapper2</a> interface.

## -struct-fields

### -field clsMedium

GUID that specifies the medium.

### -field dw1

Variable of type <b>DWORD</b> that specifies the instance of this medium. This is necessary when two identical devices are present on the host system.

### -field dw2

Not used.

## -remarks

A <i>medium</i> identifies a hardware path of communication that exists within a single hardware device or between two devices. Register mediums if your filter is built on kernel streaming pins and needs to connect to other such filters.

This structure is equivalent to the <a href="/windows-hardware/drivers/stream/kspin-medium-structure">KSPIN_MEDIUM</a> structure, which is used by kernel streaming drivers.

## -see-also

<a href="/windows/desktop/DirectShow/directshow-structures">DirectShow Structures</a>



<a href="/windows/desktop/DirectShow/ksmultiple-item">KSMULTIPLE_ITEM</a>