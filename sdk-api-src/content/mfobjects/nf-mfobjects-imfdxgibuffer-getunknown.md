---
UID: NF:mfobjects.IMFDXGIBuffer.GetUnknown
title: IMFDXGIBuffer::GetUnknown (mfobjects.h)
description: Gets an IUnknown pointer that was previously stored in the media buffer object.
helpviewer_keywords: ["GetUnknown","GetUnknown method [Media Foundation]","GetUnknown method [Media Foundation]","IMFDXGIBuffer interface","IMFDXGIBuffer interface [Media Foundation]","GetUnknown method","IMFDXGIBuffer.GetUnknown","IMFDXGIBuffer::GetUnknown","mf.imfdxgibuffer_getunknown","mfobjects/IMFDXGIBuffer::GetUnknown"]
old-location: mf\imfdxgibuffer_getunknown.htm
tech.root: mf
ms.assetid: 6B4A5E79-3A0A-439E-ABE1-F92C3D07FB57
ms.date: 12/05/2018
ms.keywords: GetUnknown, GetUnknown method [Media Foundation], GetUnknown method [Media Foundation],IMFDXGIBuffer interface, IMFDXGIBuffer interface [Media Foundation],GetUnknown method, IMFDXGIBuffer.GetUnknown, IMFDXGIBuffer::GetUnknown, mf.imfdxgibuffer_getunknown, mfobjects/IMFDXGIBuffer::GetUnknown
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
 - IMFDXGIBuffer::GetUnknown
 - mfobjects/IMFDXGIBuffer::GetUnknown
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
 - IMFDXGIBuffer.GetUnknown
---

# IMFDXGIBuffer::GetUnknown


## -description

Gets an <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> pointer that was previously stored in the media buffer object.

## -parameters

### -param guid [in]

The identifier of the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> pointer.

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
<dt><b>MF_E_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The specified key was not found.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgibuffer">IMFDXGIBuffer</a>



<a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfdxgibuffer-setunknown">IMFDXGIBuffer::SetUnknown</a>