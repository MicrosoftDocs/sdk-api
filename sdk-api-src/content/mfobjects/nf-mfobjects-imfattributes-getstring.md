---
UID: NF:mfobjects.IMFAttributes.GetString
title: IMFAttributes::GetString (mfobjects.h)
description: Retrieves a wide-character string associated with a key.
helpviewer_keywords: ["756d8fba-d372-46f9-8035-f657d7ff133f","GetString","GetString method [Media Foundation]","GetString method [Media Foundation]","IMFAttributes interface","IMFAttributes interface [Media Foundation]","GetString method","IMFAttributes.GetString","IMFAttributes::GetString","mf.imfattributes_getstring","mfobjects/IMFAttributes::GetString"]
old-location: mf\imfattributes_getstring.htm
tech.root: mf
ms.assetid: 756d8fba-d372-46f9-8035-f657d7ff133f
ms.date: 12/05/2018
ms.keywords: 756d8fba-d372-46f9-8035-f657d7ff133f, GetString, GetString method [Media Foundation], GetString method [Media Foundation],IMFAttributes interface, IMFAttributes interface [Media Foundation],GetString method, IMFAttributes.GetString, IMFAttributes::GetString, mf.imfattributes_getstring, mfobjects/IMFAttributes::GetString
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
 - IMFAttributes::GetString
 - mfobjects/IMFAttributes::GetString
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
 - IMFAttributes.GetString
---

# IMFAttributes::GetString


## -description

Retrieves a wide-character string associated with a key.

## -parameters

### -param guidKey [in]

GUID that identifies which value to retrieve. The attribute type must be <b>MF_ATTRIBUTE_STRING</b>.

### -param pwszValue [out]

Pointer to a wide-character array allocated by the caller. The array must be large enough to hold the string, including the terminating <b>NULL</b> character. If the key is found and the value is a string type, the method copies the string into this buffer. To find the length of the string, call <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstringlength">IMFAttributes::GetStringLength</a>.

### -param cchBufSize [in]

The size of the <i>pwszValue</i> array, in characters. This value includes the terminating NULL character.

### -param pcchLength [out]

Receives the number of characters in the string, excluding the terminating <b>NULL</b> character. This parameter can be <b>NULL</b>.

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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The length of the string is too large to fit in a <b>UINT32</b> value.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOT_SUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
The buffer is not large enough to hold the string.

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
The attribute value is not a string.

</td>
</tr>
</table>

## -remarks

You can also use the <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getallocatedstring">IMFAttributes::GetAllocatedString</a> method, which allocates the buffer to hold the string.

This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>

#### Examples

The following code example shows how to get an attribute whose value is a string.


```
HRESULT AttributeGetString(IMFAttributes *pAttributes)
{
    HRESULT hr = S_OK;
    UINT32 cchLength = 0;
    WCHAR *pString = NULL;

    hr = pAttributes->GetStringLength(MY_ATTRIBUTE, &cchLength);
    
    if (SUCCEEDED(hr))
    {
        pString = new WCHAR[cchLength + 1];
        if (pString == NULL)
        {
            hr = E_OUTOFMEMORY;
        }
    }

    if (SUCCEEDED(hr))
    {
        hr = pAttributes->GetString(
            MY_ATTRIBUTE, pString, cchLength + 1, &cchLength);
    }

    if (pString)
    {
        delete [] pString;
    }
    return hr;
}
```

## -see-also

<a href="/windows/desktop/medfound/attributes-and-properties">Attributes and Properties</a>



<a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a>



<a href="/windows/desktop/api/mfobjects/ne-mfobjects-mf_attribute_type">MF_ATTRIBUTE_TYPE</a>