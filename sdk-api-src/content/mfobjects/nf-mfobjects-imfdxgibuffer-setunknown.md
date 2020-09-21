---
UID: NF:mfobjects.IMFDXGIBuffer.SetUnknown
title: IMFDXGIBuffer::SetUnknown (mfobjects.h)
description: Stores an arbitrary IUnknown pointer in the media buffer object.
helpviewer_keywords: ["IMFDXGIBuffer interface [Media Foundation]","SetUnknown method","IMFDXGIBuffer.SetUnknown","IMFDXGIBuffer::SetUnknown","SetUnknown","SetUnknown method [Media Foundation]","SetUnknown method [Media Foundation]","IMFDXGIBuffer interface","mf.imfdxgibuffer_setunknown","mfobjects/IMFDXGIBuffer::SetUnknown"]
old-location: mf\imfdxgibuffer_setunknown.htm
tech.root: mf
ms.assetid: 94BA5E48-FF89-48FA-BE0D-C158A5B4D4CF
ms.date: 12/05/2018
ms.keywords: IMFDXGIBuffer interface [Media Foundation],SetUnknown method, IMFDXGIBuffer.SetUnknown, IMFDXGIBuffer::SetUnknown, SetUnknown, SetUnknown method [Media Foundation], SetUnknown method [Media Foundation],IMFDXGIBuffer interface, mf.imfdxgibuffer_setunknown, mfobjects/IMFDXGIBuffer::SetUnknown
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
 - IMFDXGIBuffer::SetUnknown
 - mfobjects/IMFDXGIBuffer::SetUnknown
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
 - IMFDXGIBuffer.SetUnknown
---

# IMFDXGIBuffer::SetUnknown


## -description

Stores an arbitrary <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> pointer in the media buffer object.

## -parameters

### -param guid [in]

The identifier for the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> pointer. This identifier is used as a key to retrieve the value. It can be any <b>GUID</b> value.

### -param pUnkData [in]

A pointer to the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. Set this parameter to <b>NULL</b> to clear a pointer that was previously set.

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
<dt><b>ERROR_OBJECT_ALREADY_EXISTS</b></dt>
</dl>
</td>
<td width="60%">
An item already exists with this key.

</td>
</tr>
</table>

## -remarks

To retrieve the pointer from the object, call <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfdxgibuffer-getunknown">IMFDXGIBuffer::GetUnknown</a>.

## -see-also

<a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgibuffer">IMFDXGIBuffer</a>



<a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfdxgibuffer-getunknown">IMFDXGIBuffer::GetUnknown</a>