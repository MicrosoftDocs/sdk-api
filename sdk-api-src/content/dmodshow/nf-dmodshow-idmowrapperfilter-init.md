---
UID: NF:dmodshow.IDMOWrapperFilter.Init
title: IDMOWrapperFilter::Init (dmodshow.h)
description: The Init method initializes the DMO Wrapper filter with the specified DMO.
helpviewer_keywords: ["IDMOWrapperFilter interface [DirectShow]","Init method","IDMOWrapperFilter.Init","IDMOWrapperFilter::Init","IDMOWrapperFilterInit","Init","Init method [DirectShow]","Init method [DirectShow]","IDMOWrapperFilter interface","dmodshow/IDMOWrapperFilter::Init","dshow.idmowrapperfilter_init"]
old-location: dshow\idmowrapperfilter_init.htm
tech.root: dshow
ms.assetid: 45f305b5-82bc-44c1-9af7-93aab371ed33
ms.date: 4/26/2023
ms.keywords: IDMOWrapperFilter interface [DirectShow],Init method, IDMOWrapperFilter.Init, IDMOWrapperFilter::Init, IDMOWrapperFilterInit, Init, Init method [DirectShow], Init method [DirectShow],IDMOWrapperFilter interface, dmodshow/IDMOWrapperFilter::Init, dshow.idmowrapperfilter_init
req.header: dmodshow.h
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
req.lib: Dmoguids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDMOWrapperFilter::Init
 - dmodshow/IDMOWrapperFilter::Init
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dmoguids.lib
 - Dmoguids.dll
api_name:
 - IDMOWrapperFilter.Init
---

# IDMOWrapperFilter::Init


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>Init</code> method initializes the DMO Wrapper filter with the specified DMO.

## -parameters

### -param clsidDMO

Class identifier (CLSID) of the DMO.

### -param catDMO

CLSID that specifies the category of the DMO.

## -returns

Returns S_OK if successful. Otherwise, returns an <b>HRESULT</b> value indicating the cause of the error.

## -remarks

In some cases, the DMO Wrapper filter performs optimizations based on the category.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/dmodshow/nn-dmodshow-idmowrapperfilter">IDMOWrapperFilter Interface</a>