---
UID: NN:strmif.IVPManager
title: IVPManager (strmif.h)
description: The IVPManager interface is implemented on the Video Port Manager (VPM).
helpviewer_keywords: ["IVPManager","IVPManager interface [DirectShow]","IVPManager interface [DirectShow]","described","IVPManagerInterface","dshow.ivpmanager","strmif/IVPManager"]
old-location: dshow\ivpmanager.htm
tech.root: dshow
ms.assetid: 9064daa7-5868-49a5-9fd6-9a332ab3b470
ms.date: 4/26/2023
ms.keywords: IVPManager, IVPManager interface [DirectShow], IVPManager interface [DirectShow],described, IVPManagerInterface, dshow.ivpmanager, strmif/IVPManager
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
 - IVPManager
 - strmif/IVPManager
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
 - IVPManager
---

# IVPManager interface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>IVPManager</code> interface is implemented on the <a href="/windows/desktop/DirectShow/video-port-manager">Video Port Manager</a> (VPM). The interface provides methods for applications to specify and retrieve indexes for ports when there are multiple video ports on a system, and to specify and retrieve the rectangle used by the video port. Currently, only the two index-related methods are implemented.

## -inheritance

The <b>IVPManager</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVPManager</b> also has these types of members:

