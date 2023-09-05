---
UID: NN:strmif.IDvdInfo
title: IDvdInfo (strmif.h)
description: Note  This interface has been deprecated. (IDvdInfo)
helpviewer_keywords: ["IDvdInfo","IDvdInfo interface [DirectShow]","IDvdInfo interface [DirectShow]","described","IDvdInfoInterface","dshow.idvdinfo","strmif/IDvdInfo"]
old-location: dshow\idvdinfo.htm
tech.root: dshow
ms.assetid: 6b0c5dfe-aa1b-4ad0-9272-f1351e494b11
ms.date: 4/26/2023
ms.keywords: IDvdInfo, IDvdInfo interface [DirectShow], IDvdInfo interface [DirectShow],described, IDvdInfoInterface, dshow.idvdinfo, strmif/IDvdInfo
req.header: strmif.h
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDvdInfo
 - strmif/IDvdInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - strmif.h
api_name:
 - IDvdInfo
---

# IDvdInfo interface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  This interface has been deprecated. It will continue to be supported for backward compatibility with existing applications, but new applications should use <a href="/windows/desktop/api/strmif/nn-strmif-idvdinfo2">IDvdInfo2</a>.</div>
<div> </div>
The <b>IDvdInfo</b> interface enables an application to query for attributes of available DVD titles and the DVD player status. It also allows for control of a DVD player beyond Annex J in the DVD specification. Use this interface to retrieve details about a DVD-Video or about the current state of the DVD player filter graph.

## -inheritance

The <b>IDvdInfo</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDvdInfo</b> also has these types of members:

## -see-also

<a href="/windows/desktop/DirectShow/deprecated-interfaces">Deprecated Interfaces</a>
