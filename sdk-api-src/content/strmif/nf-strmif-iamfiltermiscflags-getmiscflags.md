---
UID: NF:strmif.IAMFilterMiscFlags.GetMiscFlags
title: IAMFilterMiscFlags::GetMiscFlags (strmif.h)
description: The GetMiscFlags method returns the filter's type, either source or renderer.
helpviewer_keywords: ["GetMiscFlags","GetMiscFlags method [DirectShow]","GetMiscFlags method [DirectShow]","IAMFilterMiscFlags interface","IAMFilterMiscFlags interface [DirectShow]","GetMiscFlags method","IAMFilterMiscFlags.GetMiscFlags","IAMFilterMiscFlags::GetMiscFlags","IAMFilterMiscFlagsGetMiscFlags","dshow.iamfiltermiscflags_getmiscflags","strmif/IAMFilterMiscFlags::GetMiscFlags"]
old-location: dshow\iamfiltermiscflags_getmiscflags.htm
tech.root: dshow
ms.assetid: 03728d28-a3e5-4ac5-b637-1daa173e5e88
ms.date: 4/26/2023
ms.keywords: GetMiscFlags, GetMiscFlags method [DirectShow], GetMiscFlags method [DirectShow],IAMFilterMiscFlags interface, IAMFilterMiscFlags interface [DirectShow],GetMiscFlags method, IAMFilterMiscFlags.GetMiscFlags, IAMFilterMiscFlags::GetMiscFlags, IAMFilterMiscFlagsGetMiscFlags, dshow.iamfiltermiscflags_getmiscflags, strmif/IAMFilterMiscFlags::GetMiscFlags
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAMFilterMiscFlags::GetMiscFlags
 - strmif/IAMFilterMiscFlags::GetMiscFlags
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IAMFilterMiscFlags.GetMiscFlags
---

# IAMFilterMiscFlags::GetMiscFlags


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetMiscFlags</code> method returns the filter's type, either source or renderer.



## -returns

This method returns a member of the <a href="/windows/desktop/api/strmif/ne-strmif-_am_filter_misc_flags">_AM_FILTER_MISC_FLAGS</a> enumeration.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamfiltermiscflags">IAMFilterMiscFlags Interface</a>
