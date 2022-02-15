---
UID: NN:mfidl.IMFMediaSource
title: IMFMediaSource (mfidl.h)
description: Implemented by media source objects.
helpviewer_keywords: ["8b579f61-6fea-4b20-a051-7633fc01fa05","IMFMediaSource","IMFMediaSource interface [Media Foundation]","IMFMediaSource interface [Media Foundation]","described","mf.imfmediasource","mfidl/IMFMediaSource"]
old-location: mf\imfmediasource.htm
tech.root: mf
ms.assetid: 8b579f61-6fea-4b20-a051-7633fc01fa05
ms.date: 12/05/2018
ms.keywords: 8b579f61-6fea-4b20-a051-7633fc01fa05, IMFMediaSource, IMFMediaSource interface [Media Foundation], IMFMediaSource interface [Media Foundation],described, mf.imfmediasource, mfidl/IMFMediaSource
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
 - IMFMediaSource
 - mfidl/IMFMediaSource
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
 - IMFMediaSource
---

# IMFMediaSource interface


## -description

Implemented by media source objects.

Media sources are objects that generate media data. For example, the data might come from a video file, a network stream, or a hardware device, such as a camera. Each media source contains one or more streams, and each stream delivers data of one type, such as audio or video.

## -inheritance

The <b>IMFMediaSource</b> interface inherits from <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator">IMFMediaEventGenerator</a>. <b>IMFMediaSource</b> also has these types of members:

## -remarks

In Windows 8, this interface is extended with <a href="/windows/desktop/api/mfidl/nn-mfidl-imfmediasourceex">IMFMediaSourceEx</a>.

For some device sources, such as cameras or microphones, the **IMFMediaSource** also implements the [IKsControl](/windows-hardware/drivers/ddi/ksproxy/nn-ksproxy-ikscontrol) which can be used by user mode applications to issue KSPROPERTY, KSEVENT and KSMETHOD operations to the underlying device driver.

> [!NOTE] 
> This interface is optional and may not be available. If this interface is not available, [QueryInterface](../unknwn/nf-unknwn-iunknown-queryinterface(refiid_void).md) will return E_NOINTERFACE.

## -see-also

<a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator">IMFMediaEventGenerator</a>



<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>



<a href="/windows/desktop/medfound/media-sources">Media Sources</a>
