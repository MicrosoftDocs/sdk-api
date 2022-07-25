---
UID: NF:mfobjects.IMFDXGIBuffer.GetResource
title: IMFDXGIBuffer::GetResource (mfobjects.h)
description: Queries the Microsoft DirectX Graphics Infrastructure (DXGI)surface for an interface.
helpviewer_keywords: ["GetResource","GetResource method [Media Foundation]","GetResource method [Media Foundation]","IMFDXGIBuffer interface","IMFDXGIBuffer interface [Media Foundation]","GetResource method","IMFDXGIBuffer.GetResource","IMFDXGIBuffer::GetResource","mf.imfdxgibuffer_getresource","mfobjects/IMFDXGIBuffer::GetResource"]
old-location: mf\imfdxgibuffer_getresource.htm
tech.root: mf
ms.assetid: E8FF3346-D60A-4FF9-AF3E-673397EA6E6A
ms.date: 12/05/2018
ms.keywords: GetResource, GetResource method [Media Foundation], GetResource method [Media Foundation],IMFDXGIBuffer interface, IMFDXGIBuffer interface [Media Foundation],GetResource method, IMFDXGIBuffer.GetResource, IMFDXGIBuffer::GetResource, mf.imfdxgibuffer_getresource, mfobjects/IMFDXGIBuffer::GetResource
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
 - IMFDXGIBuffer::GetResource
 - mfobjects/IMFDXGIBuffer::GetResource
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
 - IMFDXGIBuffer.GetResource
---

# IMFDXGIBuffer::GetResource


## -description

Queries the Microsoft DirectX Graphics Infrastructure (DXGI)surface for an interface.

## -parameters

### -param riid [in]

The interface identifier (IID) of the interface being requested.

### -param ppvObject [out]

Receives a pointer to the interface. The caller must release the interface.

## -returns

This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b> E_NOINTERFACE</b></dt>
</dl>
</td>
<td width="60%">
The object does not support the specified interface.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_INVALIDREQUEST</b></dt>
</dl>
</td>
<td width="60%">
Invalid request.

</td>
</tr>
</table>

## -remarks

You can use this method to get a pointer to the <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11texture2d">ID3D11Texture2D</a> interface of the surface. If the buffer is locked, the method returns <b>MF_E_INVALIDREQUEST</b>.

## -see-also

<a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgibuffer">IMFDXGIBuffer</a>