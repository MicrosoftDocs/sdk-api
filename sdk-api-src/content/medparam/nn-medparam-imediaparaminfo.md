---
UID: NN:medparam.IMediaParamInfo
title: IMediaParamInfo (medparam.h)
description: The IMediaParamInfo interface retrieves information about the parameters that an object supports. The set of parameters that an object supports will not change over the lifetime of an application. To set parameter values, use the IMediaParams interface.
helpviewer_keywords: ["IMediaParamInfo","IMediaParamInfo interface [DirectShow]","IMediaParamInfo interface [DirectShow]","described","IMediaParamInfoInterface","dshow.imediaparaminfo","medparam/IMediaParamInfo"]
old-location: dshow\imediaparaminfo.htm
tech.root: dshow
ms.assetid: 80c7da71-7898-4bda-a181-09ad8906532a
ms.date: 4/26/2023
ms.keywords: IMediaParamInfo, IMediaParamInfo interface [DirectShow], IMediaParamInfo interface [DirectShow],described, IMediaParamInfoInterface, dshow.imediaparaminfo, medparam/IMediaParamInfo
req.header: medparam.h
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
req.lib: Dmoguids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMediaParamInfo
 - medparam/IMediaParamInfo
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
 - IMediaParamInfo
---

# IMediaParamInfo interface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>IMediaParamInfo</code> interface retrieves information about the parameters that an object supports. The set of parameters that an object supports will not change over the lifetime of an application. To set parameter values, use the <a href="/windows/desktop/api/medparam/nn-medparam-imediaparams">IMediaParams</a> interface.

## -inheritance

The <b>IMediaParamInfo</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMediaParamInfo</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

