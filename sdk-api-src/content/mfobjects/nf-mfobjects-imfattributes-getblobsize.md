---
UID: NF:mfobjects.IMFAttributes.GetBlobSize
title: IMFAttributes::GetBlobSize (mfobjects.h)
description: Retrieves the length of a byte array associated with a key.
helpviewer_keywords: ["93ab65e7-2168-4cfb-a871-b39554ba66e0","GetBlobSize","GetBlobSize method [Media Foundation]","GetBlobSize method [Media Foundation]","IMFAttributes interface","IMFAttributes interface [Media Foundation]","GetBlobSize method","IMFAttributes.GetBlobSize","IMFAttributes::GetBlobSize","mf.imfattributes_getblobsize","mfobjects/IMFAttributes::GetBlobSize"]
old-location: mf\imfattributes_getblobsize.htm
tech.root: mf
ms.assetid: 93ab65e7-2168-4cfb-a871-b39554ba66e0
ms.date: 12/05/2018
ms.keywords: 93ab65e7-2168-4cfb-a871-b39554ba66e0, GetBlobSize, GetBlobSize method [Media Foundation], GetBlobSize method [Media Foundation],IMFAttributes interface, IMFAttributes interface [Media Foundation],GetBlobSize method, IMFAttributes.GetBlobSize, IMFAttributes::GetBlobSize, mf.imfattributes_getblobsize, mfobjects/IMFAttributes::GetBlobSize
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
 - IMFAttributes::GetBlobSize
 - mfobjects/IMFAttributes::GetBlobSize
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
 - IMFAttributes.GetBlobSize
---

# IMFAttributes::GetBlobSize


## -description

Retrieves the length of a byte array associated with a key.

## -parameters

### -param guidKey [in]

GUID that identifies which value to retrieve. The attribute type must be <b>MF_ATTRIBUTE_BLOB</b>.

### -param pcbBlobSize [out]

If the key is found and the value is a byte array, this parameter receives the size of the array, in bytes.

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

To get the byte array, call <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob">IMFAttributes::GetBlob</a>.

This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>

## -see-also

<a href="/windows/desktop/medfound/attributes-and-properties">Attributes and Properties</a>



<a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a>



<a href="/windows/desktop/api/mfobjects/ne-mfobjects-mf_attribute_type">MF_ATTRIBUTE_TYPE</a>