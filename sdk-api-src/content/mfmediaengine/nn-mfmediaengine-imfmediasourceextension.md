---
UID: NN:mfmediaengine.IMFMediaSourceExtension
title: IMFMediaSourceExtension (mfmediaengine.h)
description: Provides functionality for the Media Source Extension (MSE).
helpviewer_keywords: ["IMFMediaSourceExtension","IMFMediaSourceExtension interface [Media Foundation]","IMFMediaSourceExtension interface [Media Foundation]","described","mf.imfmediasourceextension","mfmediaengine/IMFMediaSourceExtension"]
old-location: mf\imfmediasourceextension.htm
tech.root: mf
ms.assetid: 2acabcc2-242d-4b3d-b5b4-680c7973201f
ms.date: 12/05/2018
ms.keywords: IMFMediaSourceExtension, IMFMediaSourceExtension interface [Media Foundation], IMFMediaSourceExtension interface [Media Foundation],described, mf.imfmediasourceextension, mfmediaengine/IMFMediaSourceExtension
req.header: mfmediaengine.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mfmediaengine.idl
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
 - IMFMediaSourceExtension
 - mfmediaengine/IMFMediaSourceExtension
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfmediaengine.h
api_name:
 - IMFMediaSourceExtension
---

# IMFMediaSourceExtension interface


## -description

Provides functionality for the Media Source Extension (MSE).

## -inheritance

The <b>IMFMediaSourceExtension</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFMediaSourceExtension</b> also has these types of members:

## -remarks

  Media Source Extensions (MSE) is a World Wide Web Consortium (W3C) standard that extends the HTML5 media  elements to enable dynamically changing the media stream without the use of plug-ins. The   <b>IMFMediaSourceExtension</b> interface  and the related Microsoft Win32 API implement MSE and are expected to only be called by web browsers implementing MSE.  

The MSE media source keeps track of the ready state of the of the source as well as a list of <a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebuffer">IMFSourceBuffer</a> objects which provide media data for the source.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
