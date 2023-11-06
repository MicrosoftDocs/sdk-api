---
UID: NN:strmif.IAMPhysicalPinInfo
title: IAMPhysicalPinInfo (strmif.h)
description: Note  This interface has been deprecated. (IAMPhysicalPinInfo)
helpviewer_keywords: ["IAMPhysicalPinInfo","IAMPhysicalPinInfo interface [DirectShow]","IAMPhysicalPinInfo interface [DirectShow]","described","IAMPhysicalPinInfoInterface","dshow.iamphysicalpininfo","strmif/IAMPhysicalPinInfo"]
old-location: dshow\iamphysicalpininfo.htm
tech.root: dshow
ms.assetid: d1d05d2c-018e-421f-bfb9-810d708f726c
ms.date: 4/26/2023
ms.keywords: IAMPhysicalPinInfo, IAMPhysicalPinInfo interface [DirectShow], IAMPhysicalPinInfo interface [DirectShow],described, IAMPhysicalPinInfoInterface, dshow.iamphysicalpininfo, strmif/IAMPhysicalPinInfo
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
 - IAMPhysicalPinInfo
 - strmif/IAMPhysicalPinInfo
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
 - IAMPhysicalPinInfo
---

# IAMPhysicalPinInfo interface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  This interface has been deprecated. It will continue to be supported for backward compatibility with existing applications, but new applications and filters should not use it.</div>
<div> </div>
This interface enables an application or filter to retrieve information about a pin that represents a physical hardware connections.

## -inheritance

The <b>IAMPhysicalPinInfo</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAMPhysicalPinInfo</b> also has these types of members:

## -see-also

<a href="/windows/desktop/DirectShow/deprecated-interfaces">Deprecated Interfaces</a>
