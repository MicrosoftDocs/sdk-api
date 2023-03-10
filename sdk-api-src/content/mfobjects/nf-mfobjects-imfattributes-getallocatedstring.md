---
UID: NF:mfobjects.IMFAttributes.GetAllocatedString
title: IMFAttributes::GetAllocatedString (mfobjects.h)
description: Gets a wide-character string associated with a key. This method allocates the memory for the string.
helpviewer_keywords: ["550a3035-ea16-4784-8f69-9522259bb338","GetAllocatedString","GetAllocatedString method [Media Foundation]","GetAllocatedString method [Media Foundation]","IMFAttributes interface","IMFAttributes interface [Media Foundation]","GetAllocatedString method","IMFAttributes.GetAllocatedString","IMFAttributes::GetAllocatedString","mf.imfattributes_getallocatedstring","mfobjects/IMFAttributes::GetAllocatedString"]
old-location: mf\imfattributes_getallocatedstring.htm
tech.root: mf
ms.assetid: 550a3035-ea16-4784-8f69-9522259bb338
ms.date: 12/05/2018
ms.keywords: 550a3035-ea16-4784-8f69-9522259bb338, GetAllocatedString, GetAllocatedString method [Media Foundation], GetAllocatedString method [Media Foundation],IMFAttributes interface, IMFAttributes interface [Media Foundation],GetAllocatedString method, IMFAttributes.GetAllocatedString, IMFAttributes::GetAllocatedString, mf.imfattributes_getallocatedstring, mfobjects/IMFAttributes::GetAllocatedString
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
 - IMFAttributes::GetAllocatedString
 - mfobjects/IMFAttributes::GetAllocatedString
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
 - IMFAttributes.GetAllocatedString
---

# IMFAttributes::GetAllocatedString


## -description

Gets a wide-character string associated with a key. This method allocates the memory for the string.

## -parameters

### -param guidKey [in]

A GUID that identifies which value to retrieve. The attribute type must be <b>MF_ATTRIBUTE_STRING</b>.

### -param ppwszValue [out]

If the key is found and the value is a string type, this parameter receives a copy of the string. The caller must free the memory for the string by calling <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a>.

### -param pcchLength [out]

Receives the number of characters in the string, excluding the terminating <b>NULL</b> character. This parameter must not be <b>NULL</b>.

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
The attribute value is not a string.
              

</td>
</tr>
</table>

## -remarks

To copy a string value into a caller-allocated buffer, use the <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring">IMFAttributes::GetString</a> method.

This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>
<div class="alert"><b>Note</b>  An earlier version of the documentation incorrectly stated that the <i>pcchLength</i> parameter can be <b>NULL</b>. Setting this parameter to <b>NULL</b> might succeed in some cases, but is not guaranteed. The caller must pass a non-<b>NULL</b> pointer for this parameter.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/medfound/attributes-and-properties">Attributes and Properties</a>



<a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a>



<a href="/windows/desktop/api/mfobjects/ne-mfobjects-mf_attribute_type">MF_ATTRIBUTE_TYPE</a>