---
UID: NF:mfobjects.IMFAttributes.GetBlob
title: IMFAttributes::GetBlob (mfobjects.h)
description: Retrieves a byte array associated with a key. This method copies the array into a caller-allocated buffer.
helpviewer_keywords: ["68528db7-90df-4abe-a957-ffb8c3f12cef","GetBlob","GetBlob method [Media Foundation]","GetBlob method [Media Foundation]","IMFAttributes interface","IMFAttributes interface [Media Foundation]","GetBlob method","IMFAttributes.GetBlob","IMFAttributes::GetBlob","mf.imfattributes_getblob","mfobjects/IMFAttributes::GetBlob"]
old-location: mf\imfattributes_getblob.htm
tech.root: mf
ms.assetid: 68528db7-90df-4abe-a957-ffb8c3f12cef
ms.date: 12/05/2018
ms.keywords: 68528db7-90df-4abe-a957-ffb8c3f12cef, GetBlob, GetBlob method [Media Foundation], GetBlob method [Media Foundation],IMFAttributes interface, IMFAttributes interface [Media Foundation],GetBlob method, IMFAttributes.GetBlob, IMFAttributes::GetBlob, mf.imfattributes_getblob, mfobjects/IMFAttributes::GetBlob
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
 - IMFAttributes::GetBlob
 - mfobjects/IMFAttributes::GetBlob
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
 - IMFAttributes.GetBlob
---

# IMFAttributes::GetBlob


## -description

Retrieves a byte array associated with a key. This method copies the array into a caller-allocated buffer.

## -parameters

### -param guidKey [in]

GUID that identifies which value to retrieve. The attribute type must be <b>MF_ATTRIBUTE_BLOB</b>.

### -param pBuf [out]

Pointer to a buffer allocated by the caller. If the key is found and the value is a byte array, the method copies the array into this buffer. To find the required size of the buffer, call <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblobsize">IMFAttributes::GetBlobSize</a>.

### -param cbBufSize [in]

The size of the <i>pBuf</i> buffer, in bytes.

### -param pcbBlobSize [out]

Receives the size of the byte array. This parameter can be <b>NULL</b>.

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
<tr>
<td width="40%">
<dl>
<dt><b>E_NOT_SUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
The buffer is not large enough to the array.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_ATTRIBUTENOTFOUND</b></dt>
</dl>
</td>
<td width="60%">
The specified key was not found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_INVALIDTYPE</b></dt>
</dl>
</td>
<td width="60%">
The attribute value is not a byte array.

</td>
</tr>
</table>

## -remarks

You can also use the <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getallocatedblob">IMFAttributes::GetAllocatedBlob</a> method, which allocates the buffer to hold the byte array.

This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>

#### Examples

The following code example shows how to get an attribute whose value is a byte array.


```
HRESULT AttributeGetBlob(IMFAttributes *pAttributes)
{
    HRESULT hr = S_OK;
    UINT32 cbBlob = 0;
    BYTE *pBlob = NULL;

    hr = pAttributes->GetBlobSize(MY_ATTRIBUTE, &cbBlob);
    
    if (SUCCEEDED(hr))
    {
        pBlob = new BYTE[cbBlob];
        if (pBlob == NULL)
        {
            hr = E_OUTOFMEMORY;
        }
    }

    if (SUCCEEDED(hr))
    {
        hr = pAttributes->GetBlob(MY_ATTRIBUTE, pBlob, cbBlob, &cbBlob);
    }

    if (pBlob)
    {
        delete [] pBlob;
    }
    return hr;
}
```

## -see-also

<a href="/windows/desktop/medfound/attributes-and-properties">Attributes and Properties</a>



<a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a>



<a href="/windows/desktop/api/mfobjects/ne-mfobjects-mf_attribute_type">MF_ATTRIBUTE_TYPE</a>