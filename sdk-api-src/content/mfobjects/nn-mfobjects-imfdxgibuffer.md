---
UID: NN:mfobjects.IMFDXGIBuffer
title: IMFDXGIBuffer (mfobjects.h)
description: Represents a buffer that contains a Microsoft DirectX Graphics Infrastructure (DXGI)surface.
helpviewer_keywords: ["IMFDXGIBuffer","IMFDXGIBuffer interface [Media Foundation]","IMFDXGIBuffer interface [Media Foundation]","described","mf.imfdxgibuffer","mfobjects/IMFDXGIBuffer"]
old-location: mf\imfdxgibuffer.htm
tech.root: mf
ms.assetid: 796D7755-275D-4A0B-A34F-5D34DCEC8AC7
ms.date: 12/05/2018
ms.keywords: IMFDXGIBuffer, IMFDXGIBuffer interface [Media Foundation], IMFDXGIBuffer interface [Media Foundation],described, mf.imfdxgibuffer, mfobjects/IMFDXGIBuffer
req.header: mfobjects.h
req.include-header: Mfidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
 - IMFDXGIBuffer
 - mfobjects/IMFDXGIBuffer
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfobjects.h
api_name:
 - IMFDXGIBuffer
---

# IMFDXGIBuffer interface


## -description

Represents a buffer that contains a Microsoft DirectX Graphics Infrastructure (DXGI)surface.

## -inheritance

The <b>IMFDXGIBuffer</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFDXGIBuffer</b> also has these types of members:

## -remarks

To create a DXGImedia buffer, first create the DXGIsurface. Then call <a href="/windows/desktop/api/mfapi/nf-mfapi-mfcreatedxgisurfacebuffer">MFCreateDXGISurfaceBuffer</a>.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
