---
UID: NN:evr.IEVRTrustedVideoPlugin
title: IEVRTrustedVideoPlugin (evr.h)
description: Enables a plug-in component for the enhanced video renderer (EVR) to work with protected media.
helpviewer_keywords: ["1dcaa01c-2596-4a22-9e2a-7f0e26d58ffe","IEVRTrustedVideoPlugin","IEVRTrustedVideoPlugin interface [Media Foundation]","IEVRTrustedVideoPlugin interface [Media Foundation]","described","evr/IEVRTrustedVideoPlugin","mf.ievrtrustedvideoplugin"]
old-location: mf\ievrtrustedvideoplugin.htm
tech.root: mfarchive
ms.assetid: 1dcaa01c-2596-4a22-9e2a-7f0e26d58ffe
ms.date: 12/05/2018
ms.keywords: 1dcaa01c-2596-4a22-9e2a-7f0e26d58ffe, IEVRTrustedVideoPlugin, IEVRTrustedVideoPlugin interface [Media Foundation], IEVRTrustedVideoPlugin interface [Media Foundation],described, evr/IEVRTrustedVideoPlugin, mf.ievrtrustedvideoplugin
req.header: evr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IEVRTrustedVideoPlugin
 - evr/IEVRTrustedVideoPlugin
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IEVRTrustedVideoPlugin
archived: true
---

# IEVRTrustedVideoPlugin interface


## -description

[The component described on this page, [Enhanced Video Renderer](/windows/win32/medfound/enhanced-video-renderer), is a legacy feature. It has been superseded by the Simple Video Renderer (SVR) exposed through the [MediaPlayer](/uwp/api/windows.media.playback.mediaplayer) and [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine) components. To play video content you should send data into one of these components and allow them to instantiate the new video renderer.  These components have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** or the lower level **IMFMediaEngine** APIs to play video media in Windows instead of the EVR, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.]

Enables a plug-in component for the enhanced video renderer (EVR) to work with protected media.

To work in the protected media path (PMP), a custom EVR mixer or presenter must implement this interface. The EVR obtains a pointer to this interface by calling <b>QueryInterface</b> on the plug-in component.

This interface is required only if the plug-in is a trusted component, designed to work in the PMP. It is not required for playing clear content in an unprotected process.

## -inheritance

The <b>IEVRTrustedVideoPlugin</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEVRTrustedVideoPlugin</b> also has these types of members:

## -see-also

<a href="/windows/desktop/medfound/enhanced-video-renderer">Enhanced Video Renderer</a>



<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>



<a href="/windows/desktop/medfound/protected-media-path">Protected Media Path</a>
