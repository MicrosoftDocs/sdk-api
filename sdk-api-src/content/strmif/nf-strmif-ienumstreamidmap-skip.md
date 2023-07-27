---
UID: NF:strmif.IEnumStreamIdMap.Skip
title: IEnumStreamIdMap::Skip (strmif.h)
description: The Skip method skip the element at the specified index.
helpviewer_keywords: ["IEnumStreamIdMap interface [DirectShow]","Skip method","IEnumStreamIdMap.Skip","IEnumStreamIdMap::Skip","IEnumStreamIdMapSkip","Skip","Skip method [DirectShow]","Skip method [DirectShow]","IEnumStreamIdMap interface","dshow.ienumstreamidmap_skip","strmif/IEnumStreamIdMap::Skip"]
old-location: dshow\ienumstreamidmap_skip.htm
tech.root: dshow
ms.assetid: 54502cd5-50b2-4bd2-a13f-180bddac178a
ms.date: 4/26/2023
ms.keywords: IEnumStreamIdMap interface [DirectShow],Skip method, IEnumStreamIdMap.Skip, IEnumStreamIdMap::Skip, IEnumStreamIdMapSkip, Skip, Skip method [DirectShow], Skip method [DirectShow],IEnumStreamIdMap interface, dshow.ienumstreamidmap_skip, strmif/IEnumStreamIdMap::Skip
req.header: strmif.h
req.include-header: Dshow.h
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
req.lib: Strmiids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IEnumStreamIdMap::Skip
 - strmif/IEnumStreamIdMap::Skip
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
 - IEnumStreamIdMap.Skip
---

# IEnumStreamIdMap::Skip


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>Skip</code> method skip the element at the specified index.

## -parameters

### -param cRecords [in]

Index of the element to skip.

## -returns

Returns S_OK if successful. If the method fails, an <b>HRESULT</b> error code is returned.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-ienumstreamidmap">IEnumStreamIdMap Interface</a>