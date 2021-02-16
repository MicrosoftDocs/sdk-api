---
UID: NF:mfidl.IMFSampleProtection.InitOutputProtection
title: IMFSampleProtection::InitOutputProtection (mfidl.h)
description: Retrieves initialization information for sample protection from the upstream component.
helpviewer_keywords: ["03bee13d-1c51-4b26-98bb-bac15264aa54","IMFSampleProtection interface [Media Foundation]","InitOutputProtection method","IMFSampleProtection.InitOutputProtection","IMFSampleProtection::InitOutputProtection","InitOutputProtection","InitOutputProtection method [Media Foundation]","InitOutputProtection method [Media Foundation]","IMFSampleProtection interface","mf.imfsampleprotection_initoutputprotection","mfidl/IMFSampleProtection::InitOutputProtection"]
old-location: mf\imfsampleprotection_initoutputprotection.htm
tech.root: mf
ms.assetid: 03bee13d-1c51-4b26-98bb-bac15264aa54
ms.date: 12/05/2018
ms.keywords: 03bee13d-1c51-4b26-98bb-bac15264aa54, IMFSampleProtection interface [Media Foundation],InitOutputProtection method, IMFSampleProtection.InitOutputProtection, IMFSampleProtection::InitOutputProtection, InitOutputProtection, InitOutputProtection method [Media Foundation], InitOutputProtection method [Media Foundation],IMFSampleProtection interface, mf.imfsampleprotection_initoutputprotection, mfidl/IMFSampleProtection::InitOutputProtection
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
 - IMFSampleProtection::InitOutputProtection
 - mfidl/IMFSampleProtection::InitOutputProtection
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
 - IMFSampleProtection.InitOutputProtection
---

# IMFSampleProtection::InitOutputProtection


## -description

Retrieves initialization information for sample protection from the upstream component.

## -parameters

### -param dwVersion [in]

Specifies the version number of the sample protection scheme. The version number is specified as a <a href="/windows/desktop/api/mfidl/ne-mfidl-sample_protection_version">SAMPLE_PROTECTION_VERSION</a> enumeration value.

### -param dwOutputId [in]

Identifier of the output stream. The identifier corresponds to the output stream identifier returned by the <a href="/windows/desktop/api/mftransform/nn-mftransform-imftransform">IMFTransform</a> interface.

### -param pbCert [in]

Pointer to a certificate provided by the downstream component.

### -param cbCert [in]

Size of the certificate, in bytes.

### -param ppbSeed [out]

Receives a pointer to a buffer that contains the initialization information for downstream component. The caller must free the memory for the buffer by calling <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a>.

### -param pcbSeed [out]

Receives the size of the <i>ppbSeed</i> buffer, in bytes.

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
Not implemented.

</td>
</tr>
</table>

## -remarks

This method must be implemented by the upstream component. The method fails if the component does not support the requested sample protection version. Downstream components do not implement this method and should return E_NOTIMPL.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfsampleprotection">IMFSampleProtection</a>