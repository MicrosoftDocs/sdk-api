---
UID: NF:bdaiface.IMPEG2PIDMap.MapPID
title: IMPEG2PIDMap::MapPID (bdaiface.h)
description: The MapPID method maps one or more PIDs to the pin.
helpviewer_keywords: ["IMPEG2PIDMap interface [DirectShow]","MapPID method","IMPEG2PIDMap.MapPID","IMPEG2PIDMap::MapPID","IMPEG2PIDMapMapPID","MapPID","MapPID method [DirectShow]","MapPID method [DirectShow]","IMPEG2PIDMap interface","bdaiface/IMPEG2PIDMap::MapPID","dshow.impeg2pidmap_mappid"]
old-location: dshow\impeg2pidmap_mappid.htm
tech.root: dshow
ms.assetid: 22784e4a-2b02-4fc9-ba55-8c918ea38892
ms.date: 4/26/2023
ms.keywords: IMPEG2PIDMap interface [DirectShow],MapPID method, IMPEG2PIDMap.MapPID, IMPEG2PIDMap::MapPID, IMPEG2PIDMapMapPID, MapPID, MapPID method [DirectShow], MapPID method [DirectShow],IMPEG2PIDMap interface, bdaiface/IMPEG2PIDMap::MapPID, dshow.impeg2pidmap_mappid
req.header: bdaiface.h
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
req.lib: Strmiids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMPEG2PIDMap::MapPID
 - bdaiface/IMPEG2PIDMap::MapPID
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
 - IMPEG2PIDMap.MapPID
---

# IMPEG2PIDMap::MapPID


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>MapPID</code> method maps one or more PIDs to the pin.

## -parameters

### -param culPID [in]

The number of elements in the <i>pulPID</i> array.

### -param pulPID [in]

Pointer to an array of size <i>culPID</i>, allocated by the caller. Each element in the array contains a PID to be mapped.

### -param MediaSampleContent [in]

Variable of type <a href="/windows/desktop/DirectShow/media-sample-content">MEDIA_SAMPLE_CONTENT</a> that specifies the contents of the stream.

## -returns

Returns S_OK if successful. If the method fails, it returns an <b>HRESULT</b> error code.

## -remarks

There may be no more than 255 distinct PIDs mapped at any given time. This includes the PIDs that the Demux maps internally for its own use; this number varies depending on the transport stream. This limitation should not present a problem in practice, because applications will typically map no more than a dozen PIDs on any given transport stream.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/previous-versions/windows/desktop/api/bdaiface/nn-bdaiface-impeg2pidmap">IMPEG2PIDMap Interface</a>