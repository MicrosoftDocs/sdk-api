---
UID: NN:dxva2api.IDirectXVideoMemoryConfiguration
title: IDirectXVideoMemoryConfiguration (dxva2api.h)
description: Sets the type of video memory for uncompressed video surfaces.
helpviewer_keywords: ["IDirectXVideoMemoryConfiguration","IDirectXVideoMemoryConfiguration interface [Media Foundation]","IDirectXVideoMemoryConfiguration interface [Media Foundation]","described","cc2a6180-9698-460a-9a0d-1ee9e15f197f","dxva2api/IDirectXVideoMemoryConfiguration","mf.idirectxvideomemoryconfiguration"]
old-location: mf\idirectxvideomemoryconfiguration.htm
tech.root: mf
ms.assetid: cc2a6180-9698-460a-9a0d-1ee9e15f197f
ms.date: 12/05/2018
ms.keywords: IDirectXVideoMemoryConfiguration, IDirectXVideoMemoryConfiguration interface [Media Foundation], IDirectXVideoMemoryConfiguration interface [Media Foundation],described, cc2a6180-9698-460a-9a0d-1ee9e15f197f, dxva2api/IDirectXVideoMemoryConfiguration, mf.idirectxvideomemoryconfiguration
req.header: dxva2api.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDirectXVideoMemoryConfiguration
 - dxva2api/IDirectXVideoMemoryConfiguration
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dxva2api.h
api_name:
 - IDirectXVideoMemoryConfiguration
---

# IDirectXVideoMemoryConfiguration interface


## -description

Sets the type of video memory for uncompressed video surfaces. This interface is used by video decoders and transforms.

The DirectShow enhanced video renderer (EVR) filter exposes this interface as a service on the filter's input pins. To obtain a pointer to this interface, call <a href="/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice">IMFGetService::GetService</a> with the service identifier MR_VIDEO_ACCELERATION_SERVICE.

A video decoder can use this interface to enumerate the EVR filter's preferred surface types and then select the surface type. The decoder should then create surfaces of that type to hold the results of the decoding operation.

This interface does not define a way to clear the surface type. In the case of DirectShow, disconnecting two filters invalidates the surface type.

## -inheritance

The <b>IDirectXVideoMemoryConfiguration</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDirectXVideoMemoryConfiguration</b> also has these types of members:

## -see-also

<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>



<a href="/windows/desktop/medfound/supporting-dxva-2-0-in-directshow">Supporting DXVA 2.0 in DirectShow</a>
