---
UID: NF:mfidl.IMFMetadata.GetLanguage
title: IMFMetadata::GetLanguage (mfidl.h)
description: Gets the current language setting.
helpviewer_keywords: ["75295c93-a389-42c4-aa56-debc36a5f532","GetLanguage","GetLanguage method [Media Foundation]","GetLanguage method [Media Foundation]","IMFMetadata interface","IMFMetadata interface [Media Foundation]","GetLanguage method","IMFMetadata.GetLanguage","IMFMetadata::GetLanguage","mf.imfmetadata_getlanguage","mfidl/IMFMetadata::GetLanguage"]
old-location: mf\imfmetadata_getlanguage.htm
tech.root: mf
ms.assetid: 75295c93-a389-42c4-aa56-debc36a5f532
ms.date: 12/05/2018
ms.keywords: 75295c93-a389-42c4-aa56-debc36a5f532, GetLanguage, GetLanguage method [Media Foundation], GetLanguage method [Media Foundation],IMFMetadata interface, IMFMetadata interface [Media Foundation],GetLanguage method, IMFMetadata.GetLanguage, IMFMetadata::GetLanguage, mf.imfmetadata_getlanguage, mfidl/IMFMetadata::GetLanguage
req.header: mfidl.h
req.include-header: 
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
 - IMFMetadata::GetLanguage
 - mfidl/IMFMetadata::GetLanguage
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
 - IMFMetadata.GetLanguage
---

# IMFMetadata::GetLanguage


## -description

Gets the current language setting.

## -parameters

### -param ppwszRFC1766 [out]

Receives a pointer to a null-terminated string containing an RFC 1766-compliant language tag. The caller must release the string by calling <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a>.

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
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The metadata provider does not support multiple languages.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_INVALIDREQUEST</b></dt>
</dl>
</td>
<td width="60%">
No language was set.
              

</td>
</tr>
</table>

## -remarks

For more information about language tags, see RFC 1766, "Tags for the Identification of Languages."

The <a href="/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-setlanguage">IMFMetadata::SetLanguage</a> and <a href="/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-getproperty">IMFMetadata::GetProperty</a> methods set and get metadata for the current language setting.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfmetadata">IMFMetadata</a>



<a href="/windows/desktop/medfound/media-metadata">Media Metadata</a>