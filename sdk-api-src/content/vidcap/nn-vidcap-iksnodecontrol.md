---
UID: NN:vidcap.IKsNodeControl
title: IKsNodeControl (vidcap.h)
description: The IKsNodeControl interface must be implemented by USB Video Class (UVC) extension units.
helpviewer_keywords: ["IKsNodeControl","IKsNodeControl interface [DirectShow]","IKsNodeControl interface [DirectShow]","described","IKsNodeControlInterface","dshow.iksnodecontrol","vidcap/IKsNodeControl"]
old-location: dshow\iksnodecontrol.htm
tech.root: dshow
ms.assetid: c38ce847-726a-4c1a-9276-810385af6c9f
ms.date: 4/26/2023
ms.keywords: IKsNodeControl, IKsNodeControl interface [DirectShow], IKsNodeControl interface [DirectShow],described, IKsNodeControlInterface, dshow.iksnodecontrol, vidcap/IKsNodeControl
req.header: vidcap.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IKsNodeControl
 - vidcap/IKsNodeControl
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Vidcap.h
api_name:
 - IKsNodeControl
---

# IKsNodeControl interface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>IKsNodeControl</code> interface must be implemented by USB Video Class (UVC) extension units. A UVC extension unit is a COM object that provides extended functionality to a USB video device, beyond the functionality provided by the UVC class driver.

The <code>IKsNodeControl</code> interface is used by the KsProxy filter to communicate with the extension unit. Applications do not use this interface. For more information, see the topic "USB Video Class Extension Units" in the Windows DDK.

## -inheritance

The <b>IKsNodeControl</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IKsNodeControl</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

