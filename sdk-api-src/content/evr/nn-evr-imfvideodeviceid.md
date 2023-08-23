---
UID: NN:evr.IMFVideoDeviceID
title: IMFVideoDeviceID (evr.h)
description: Returns the device identifier supported by a video renderer component.
helpviewer_keywords: ["IMFVideoDeviceID","IMFVideoDeviceID interface [Media Foundation]","IMFVideoDeviceID interface [Media Foundation]","described","c42b75f9-6b72-4aab-92f2-3361ab475ce9","evr/IMFVideoDeviceID","mf.imfvideodeviceid"]
old-location: mf\imfvideodeviceid.htm
tech.root: mf
ms.assetid: c42b75f9-6b72-4aab-92f2-3361ab475ce9
ms.date: 12/05/2018
ms.keywords: IMFVideoDeviceID, IMFVideoDeviceID interface [Media Foundation], IMFVideoDeviceID interface [Media Foundation],described, c42b75f9-6b72-4aab-92f2-3361ab475ce9, evr/IMFVideoDeviceID, mf.imfvideodeviceid
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
req.lib: Strmiids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFVideoDeviceID
 - evr/IMFVideoDeviceID
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - strmiids.lib
 - strmiids.dll
api_name:
 - IMFVideoDeviceID
archived: true
---

# IMFVideoDeviceID interface


## -description

Returns the device identifier supported by a video renderer component. This interface is implemented by mixers and presenters for the enhanced video renderer (EVR). If you replace either of these components, the mixer and presenter must report the same device identifier.

## -inheritance

The <b>IMFVideoDeviceID</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFVideoDeviceID</b> also has these types of members:

## -see-also

<a href="/windows/desktop/medfound/enhanced-video-renderer">Enhanced Video Renderer</a>



<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
