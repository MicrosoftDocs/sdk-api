---
UID: NF:mfobjects.IMFAttributes.GetItem
title: IMFAttributes::GetItem (mfobjects.h)
description: Retrieves the value associated with a key.
helpviewer_keywords: ["8cc4e529-d5a0-4342-82ac-ae5b28bfd61d","GetItem","GetItem method [Media Foundation]","GetItem method [Media Foundation]","IMFAttributes interface","IMFAttributes interface [Media Foundation]","GetItem method","IMFAttributes.GetItem","IMFAttributes::GetItem","mf.imfattributes_getitem","mfobjects/IMFAttributes::GetItem"]
old-location: mf\imfattributes_getitem.htm
tech.root: mf
ms.assetid: 8cc4e529-d5a0-4342-82ac-ae5b28bfd61d
ms.date: 12/05/2018
ms.keywords: 8cc4e529-d5a0-4342-82ac-ae5b28bfd61d, GetItem, GetItem method [Media Foundation], GetItem method [Media Foundation],IMFAttributes interface, IMFAttributes interface [Media Foundation],GetItem method, IMFAttributes.GetItem, IMFAttributes::GetItem, mf.imfattributes_getitem, mfobjects/IMFAttributes::GetItem
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
 - IMFAttributes::GetItem
 - mfobjects/IMFAttributes::GetItem
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
 - IMFAttributes.GetItem
---

# IMFAttributes::GetItem


## -description

Retrieves the value associated with a key.

## -parameters

### -param guidKey [in]

A GUID that identifies which value to retrieve.

### -param pValue [in, out]

A pointer to a <b>PROPVARIANT</b> that receives the value. The method fills the <b>PROPVARIANT</b> with a copy of the stored value, if the value is found. Call <b>PropVariantClear</b> to free the memory allocated by this method. This parameter can be <b>NULL</b>. If this parameter is <b>NULL</b>, the method searches for the key and returns S_OK if the key is found, but does not copy the value.

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
<dt><b>MF_E_ATTRIBUTENOTFOUND</b></dt>
</dl>
</td>
<td width="60%">
The specified key was not found.
              

</td>
</tr>
</table>

## -remarks

This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>

#### Examples

The following example copies an attribute from one attribute store to another.


```cpp
HRESULT CopyAttribute(IMFAttributes *pFrom, IMFAttributes *pTo, REFGUID guidKey)
{
    PROPVARIANT val;

    HRESULT hr = pFrom->GetItem(guidKey, &val);

    if (SUCCEEDED(hr))
    {
        hr = pTo->SetItem(guidKey, val);
        PropVariantClear(&val);
    }
    else if (hr == MF_E_ATTRIBUTENOTFOUND)
    {
        hr = S_OK;
    }
    return hr;
}

```

## -see-also

<a href="/windows/desktop/medfound/attributes-and-properties">Attributes and Properties</a>



<a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a>