---
UID: NF:mediaobj.IEnumDMO.Skip
title: IEnumDMO::Skip (mediaobj.h)
description: The Skip method skips over a specified number of items in the enumeration sequence.
helpviewer_keywords: ["IEnumDMO interface [DirectShow]","Skip method","IEnumDMO.Skip","IEnumDMO::Skip","IEnumDMOSkip","Skip","Skip method [DirectShow]","Skip method [DirectShow]","IEnumDMO interface","dshow.ienumdmo_skip","mediaobj/IEnumDMO::Skip"]
old-location: dshow\ienumdmo_skip.htm
tech.root: dshow
ms.assetid: 32722190-52b5-468a-91d6-a828ad02b203
ms.date: 4/26/2023
ms.keywords: IEnumDMO interface [DirectShow],Skip method, IEnumDMO.Skip, IEnumDMO::Skip, IEnumDMOSkip, Skip, Skip method [DirectShow], Skip method [DirectShow],IEnumDMO interface, dshow.ienumdmo_skip, mediaobj/IEnumDMO::Skip
req.header: mediaobj.h
req.include-header: Dmo.h
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
req.lib: Dmoguids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IEnumDMO::Skip
 - mediaobj/IEnumDMO::Skip
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
 - IEnumDMO.Skip
---

# IEnumDMO::Skip


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>Skip</code> method skips over a specified number of items in the enumeration sequence.

## -parameters

### -param cItemsToSkip

Number of items to skip.

## -returns

Returns S_OK if the number items skipped equals <i>cItemsToSkip</i>. Otherwise, returns S_FALSE.

## -see-also

<a href="/windows/desktop/api/mediaobj/nn-mediaobj-ienumdmo">IEnumDMO Interface</a>