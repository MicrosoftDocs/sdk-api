---
UID: NF:mfobjects.IMFDXGIBuffer.GetSubresourceIndex
title: IMFDXGIBuffer::GetSubresourceIndex (mfobjects.h)
description: Gets the index of the subresource that is associated with this media buffer.
helpviewer_keywords: ["GetSubresourceIndex","GetSubresourceIndex method [Media Foundation]","GetSubresourceIndex method [Media Foundation]","IMFDXGIBuffer interface","IMFDXGIBuffer interface [Media Foundation]","GetSubresourceIndex method","IMFDXGIBuffer.GetSubresourceIndex","IMFDXGIBuffer::GetSubresourceIndex","mf.imfdxgibuffer_getsubresourceindex","mfobjects/IMFDXGIBuffer::GetSubresourceIndex"]
old-location: mf\imfdxgibuffer_getsubresourceindex.htm
tech.root: medfound
ms.assetid: 71FA2B1C-2F11-45E7-8211-92A129F8C991
ms.date: 12/05/2018
ms.keywords: GetSubresourceIndex, GetSubresourceIndex method [Media Foundation], GetSubresourceIndex method [Media Foundation],IMFDXGIBuffer interface, IMFDXGIBuffer interface [Media Foundation],GetSubresourceIndex method, IMFDXGIBuffer.GetSubresourceIndex, IMFDXGIBuffer::GetSubresourceIndex, mf.imfdxgibuffer_getsubresourceindex, mfobjects/IMFDXGIBuffer::GetSubresourceIndex
f1_keywords:
- mfobjects/IMFDXGIBuffer.GetSubresourceIndex
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- mfobjects.h
api_name:
- IMFDXGIBuffer.GetSubresourceIndex
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFDXGIBuffer::GetSubresourceIndex


## -description


Gets the index of the subresource that is associated with this media buffer.


## -parameters




### -param puSubresource [out]

Receives the zero-based index of the subresource.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The subresource index is specified when you create the media buffer object. See <a href="https://docs.microsoft.com/windows/desktop/api/mfapi/nf-mfapi-mfcreatedxgisurfacebuffer">MFCreateDXGISurfaceBuffer</a>.

For more information about texture subresources, see <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createtexture2d">ID3D11Device::CreateTexture2D</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgibuffer">IMFDXGIBuffer</a>
 

 

