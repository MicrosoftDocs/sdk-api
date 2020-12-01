---
UID: NF:mfobjects.IMFAttributes.SetBlob
title: IMFAttributes::SetBlob (mfobjects.h)
description: Associates a byte array with a key.
helpviewer_keywords: ["4a2a25a9-4dea-40c8-988c-9e3806c8f31c","IMFAttributes interface [Media Foundation]","SetBlob method","IMFAttributes.SetBlob","IMFAttributes::SetBlob","SetBlob","SetBlob method [Media Foundation]","SetBlob method [Media Foundation]","IMFAttributes interface","mf.imfattributes_setblob","mfobjects/IMFAttributes::SetBlob"]
old-location: mf\imfattributes_setblob.htm
tech.root: mf
ms.assetid: 4a2a25a9-4dea-40c8-988c-9e3806c8f31c
ms.date: 12/05/2018
ms.keywords: 4a2a25a9-4dea-40c8-988c-9e3806c8f31c, IMFAttributes interface [Media Foundation],SetBlob method, IMFAttributes.SetBlob, IMFAttributes::SetBlob, SetBlob, SetBlob method [Media Foundation], SetBlob method [Media Foundation],IMFAttributes interface, mf.imfattributes_setblob, mfobjects/IMFAttributes::SetBlob
req.header: mfobjects.h
req.include-header: Mfidl.h
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
 - IMFAttributes::SetBlob
 - mfobjects/IMFAttributes::SetBlob
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
 - IMFAttributes.SetBlob
---

# IMFAttributes::SetBlob


## -description

Associates a byte array with a key.

## -parameters

### -param guidKey [in]

GUID that identifies the value to set. If this key already exists, the method overwrites the old value.

### -param pBuf [in]

Pointer to a byte array to associate with this key. The method stores a copy of the array.

### -param cbBufSize [in]

Size of the array, in bytes.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
The method succeeded.

</td>
</tr>
</table>

## -remarks

To retrieve the byte array, call <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob">IMFAttributes::GetBlob</a> or <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getallocatedblob">IMFAttributes::GetAllocatedBlob</a>.

This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>

## -see-also

<a href="/windows/desktop/medfound/attributes-and-properties">Attributes and Properties</a>



<a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a>