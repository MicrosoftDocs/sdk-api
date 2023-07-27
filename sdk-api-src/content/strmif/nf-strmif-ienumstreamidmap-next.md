---
UID: NF:strmif.IEnumStreamIdMap.Next
title: IEnumStreamIdMap::Next (strmif.h)
description: The Next method retrieves the next n elements in the collection.
helpviewer_keywords: ["IEnumStreamIdMap interface [DirectShow]","Next method","IEnumStreamIdMap.Next","IEnumStreamIdMap::Next","IEnumStreamIdMapNext","Next","Next method [DirectShow]","Next method [DirectShow]","IEnumStreamIdMap interface","dshow.ienumstreamidmap_next","strmif/IEnumStreamIdMap::Next"]
old-location: dshow\ienumstreamidmap_next.htm
tech.root: dshow
ms.assetid: 49e7ab23-e57e-4437-a195-88bccb6002de
ms.date: 4/26/2023
ms.keywords: IEnumStreamIdMap interface [DirectShow],Next method, IEnumStreamIdMap.Next, IEnumStreamIdMap::Next, IEnumStreamIdMapNext, Next, Next method [DirectShow], Next method [DirectShow],IEnumStreamIdMap interface, dshow.ienumstreamidmap_next, strmif/IEnumStreamIdMap::Next
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
 - IEnumStreamIdMap::Next
 - strmif/IEnumStreamIdMap::Next
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
 - IEnumStreamIdMap.Next
---

# IEnumStreamIdMap::Next


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>Next</code> method retrieves the next <i>n</i> elements in the collection.

## -parameters

### -param cRequest [in]

The number of elements to retrieve.

### -param pStreamIdMap [in, out]

Address of a user-allocated array containing <i>cRequest</i> elements that will receive the retrieved <a href="/windows/desktop/api/strmif/ns-strmif-stream_id_map">STREAM_ID_MAP</a> structures.

### -param pcReceived [out]

Receives the number of elements actually retrieved.

## -returns

Returns S_OK if successful. If the method fails,an <b>HRESULT</b> error code is returned.

## -remarks

If <i>cRequest</i> &gt;= 0 and <i>pcReceived</i> is not <b>NULL</b>, upon return <i>pcReceived</i> contains the number of stream ID maps remaining in the collection.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-ienumstreamidmap">IEnumStreamIdMap Interface</a>