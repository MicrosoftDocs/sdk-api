---
UID: NN:wmcodecdsp.IWMCodecProps
title: IWMCodecProps (wmcodecdsp.h)
description: Provides methods that retrieve format-specific codec properties.
helpviewer_keywords: ["IWMCodecProps","IWMCodecProps interface [Media Foundation]","IWMCodecProps interface [Media Foundation]","described","codecapi.iwmcodecpropsinterface","mf.iwmcodecprops","mf.iwmcodecpropsinterface","wmcodecdsp/IWMCodecProps"]
old-location: mf\iwmcodecpropsinterface.htm
tech.root: mf
ms.assetid: b49e506b-8c87-44b9-be6c-b9a33f6c9ecb
ms.date: 12/05/2018
ms.keywords: IWMCodecProps, IWMCodecProps interface [Media Foundation], IWMCodecProps interface [Media Foundation],described, codecapi.iwmcodecpropsinterface, mf.iwmcodecprops, mf.iwmcodecpropsinterface, wmcodecdsp/IWMCodecProps
req.header: wmcodecdsp.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMCodecProps
 - wmcodecdsp/IWMCodecProps
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmcodecdsp.h
api_name:
 - IWMCodecProps
---

# IWMCodecProps interface


## -description

Provides methods that retrieve format-specific codec properties.

This interface is implemented by the video encoder objects. You can obtain a pointer to <a href="/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmcodecprops">IWMCodecProps</a> by calling the <b>QueryInterface</b> method of any other interface on the object, such as <a href="/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject">IMediaObject</a> or <a href="/windows/desktop/api/mftransform/nn-mftransform-imftransform">IMFTransform</a>.

This interface enables you to receive information about a specific media type that is supported by a video encoder.

## -inheritance

The <b>IWMCodecProps</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMCodecProps</b> also has these types of members:

## -see-also

<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
