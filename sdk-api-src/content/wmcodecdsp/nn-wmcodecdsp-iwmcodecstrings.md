---
UID: NN:wmcodecdsp.IWMCodecStrings
title: IWMCodecStrings (wmcodecdsp.h)
description: Retrieves names and descriptive strings for codecs and formats.
helpviewer_keywords: ["IWMCodecStrings","IWMCodecStrings interface [Media Foundation]","IWMCodecStrings interface [Media Foundation]","described","codecapi.iwmcodecstringsinterface","mf.iwmcodecstringsinterface","wmcodecdsp/IWMCodecStrings"]
old-location: mf\iwmcodecstringsinterface.htm
tech.root: mf
ms.assetid: 84b6223e-d42a-47b0-8553-2b4d69de2da3
ms.date: 12/05/2018
ms.keywords: IWMCodecStrings, IWMCodecStrings interface [Media Foundation], IWMCodecStrings interface [Media Foundation],described, codecapi.iwmcodecstringsinterface, mf.iwmcodecstringsinterface, wmcodecdsp/IWMCodecStrings
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
 - IWMCodecStrings
 - wmcodecdsp/IWMCodecStrings
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
 - IWMCodecStrings
---

# IWMCodecStrings interface


## -description

Retrieves names and descriptive strings for codecs and formats.

This interface is implemented by all of the codec encoder objects. You can retrieve a pointer to the <b>IWMCodecStrings</b> interface for any encoder by calling the <b>QueryInterface</b> method of any other interface on the object, such as <a href="/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject">IMediaObject</a> or <a href="/windows/desktop/api/mftransform/nn-mftransform-imftransform">IMFTransform</a>, This interface is not implemented on any of the decoder DMOs.

## -inheritance

The <b>IWMCodecStrings</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMCodecStrings</b> also has these types of members:

## -see-also

<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
