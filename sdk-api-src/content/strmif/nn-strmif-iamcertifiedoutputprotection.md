---
UID: NN:strmif.IAMCertifiedOutputProtection
title: IAMCertifiedOutputProtection (strmif.h)
description: The IAMCertifiedOutputProtection interface sends Certified Output Protection Protocol (COPP) messages to the graphics driver.
helpviewer_keywords: ["IAMCertifiedOutputProtection","IAMCertifiedOutputProtection interface [DirectShow]","IAMCertifiedOutputProtection interface [DirectShow]","described","IAMCertifiedOutputProtectionInterface","dshow.iamcertifiedoutputprotection","strmif/IAMCertifiedOutputProtection"]
old-location: dshow\iamcertifiedoutputprotection.htm
tech.root: dshow
ms.assetid: e5da271d-9528-4bcb-8b76-56fbec2e5855
ms.date: 4/26/2023
ms.keywords: IAMCertifiedOutputProtection, IAMCertifiedOutputProtection interface [DirectShow], IAMCertifiedOutputProtection interface [DirectShow],described, IAMCertifiedOutputProtectionInterface, dshow.iamcertifiedoutputprotection, strmif/IAMCertifiedOutputProtection
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 R2 [desktop apps only]
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
 - IAMCertifiedOutputProtection
 - strmif/IAMCertifiedOutputProtection
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
 - IAMCertifiedOutputProtection
---

# IAMCertifiedOutputProtection interface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>IAMCertifiedOutputProtection</code> interface sends Certified Output Protection Protocol (COPP) messages to the graphics driver. This interface is exposed by the Video Mixing Renderer 7 (VMR-7) and Video Mixing Renderer 9 (VMR-9) filters.

For information about using COPP, see <a href="/windows/desktop/DirectShow/using-certified-output-protection-protocol--copp">Using Certified Output Protection Protocol (COPP)</a>.

## -inheritance

The <b>IAMCertifiedOutputProtection</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAMCertifiedOutputProtection</b> also has these types of members:

## -see-also

<a href="/windows/desktop/DirectShow/interfaces">Interfaces</a>
