---
UID: NF:mfidl.IMFMediaSourceEx.SetD3DManager
title: IMFMediaSourceEx::SetD3DManager (mfidl.h)
description: Sets a pointer to the Microsoft DirectX Graphics Infrastructure (DXGI) Device Manager on the media source.
helpviewer_keywords: ["IMFMediaSourceEx interface [Media Foundation]","SetD3DManager method","IMFMediaSourceEx.SetD3DManager","IMFMediaSourceEx::SetD3DManager","SetD3DManager","SetD3DManager method [Media Foundation]","SetD3DManager method [Media Foundation]","IMFMediaSourceEx interface","mf.imfmediasourceex_setd3dmanager","mfidl/IMFMediaSourceEx::SetD3DManager"]
old-location: mf\imfmediasourceex_setd3dmanager.htm
tech.root: mf
ms.assetid: 9E956E68-9950-4AA1-BF43-C1DCB02393F7
ms.date: 12/05/2018
ms.keywords: IMFMediaSourceEx interface [Media Foundation],SetD3DManager method, IMFMediaSourceEx.SetD3DManager, IMFMediaSourceEx::SetD3DManager, SetD3DManager, SetD3DManager method [Media Foundation], SetD3DManager method [Media Foundation],IMFMediaSourceEx interface, mf.imfmediasourceex_setd3dmanager, mfidl/IMFMediaSourceEx::SetD3DManager
req.header: mfidl.h
req.include-header: 
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
 - IMFMediaSourceEx::SetD3DManager
 - mfidl/IMFMediaSourceEx::SetD3DManager
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfidl.h
api_name:
 - IMFMediaSourceEx.SetD3DManager
---

# IMFMediaSourceEx::SetD3DManager


## -description

Sets a pointer to the Microsoft DirectX Graphics Infrastructure (DXGI) Device Manager on the media source.

## -parameters

### -param pManager [in]

A pointer to the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface of the DXGI Manager. The media source should query this pointer for the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager">IMFDXGIDeviceManager</a> interface.

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
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The media source does not support source-level attributes.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfmediasourceex">IMFMediaSourceEx</a>