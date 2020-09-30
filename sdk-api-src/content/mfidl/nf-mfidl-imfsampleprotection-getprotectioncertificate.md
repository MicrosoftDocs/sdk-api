---
UID: NF:mfidl.IMFSampleProtection.GetProtectionCertificate
title: IMFSampleProtection::GetProtectionCertificate (mfidl.h)
description: Retrieves the sample protection certificate.
helpviewer_keywords: ["GetProtectionCertificate","GetProtectionCertificate method [Media Foundation]","GetProtectionCertificate method [Media Foundation]","IMFSampleProtection interface","IMFSampleProtection interface [Media Foundation]","GetProtectionCertificate method","IMFSampleProtection.GetProtectionCertificate","IMFSampleProtection::GetProtectionCertificate","b93ecc4e-40f6-4ae1-9a1a-9767e6c8c4af","mf.imfsampleprotection_getprotectioncertificate","mfidl/IMFSampleProtection::GetProtectionCertificate"]
old-location: mf\imfsampleprotection_getprotectioncertificate.htm
tech.root: mf
ms.assetid: b93ecc4e-40f6-4ae1-9a1a-9767e6c8c4af
ms.date: 12/05/2018
ms.keywords: GetProtectionCertificate, GetProtectionCertificate method [Media Foundation], GetProtectionCertificate method [Media Foundation],IMFSampleProtection interface, IMFSampleProtection interface [Media Foundation],GetProtectionCertificate method, IMFSampleProtection.GetProtectionCertificate, IMFSampleProtection::GetProtectionCertificate, b93ecc4e-40f6-4ae1-9a1a-9767e6c8c4af, mf.imfsampleprotection_getprotectioncertificate, mfidl/IMFSampleProtection::GetProtectionCertificate
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
 - IMFSampleProtection::GetProtectionCertificate
 - mfidl/IMFSampleProtection::GetProtectionCertificate
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
 - IMFSampleProtection.GetProtectionCertificate
---

# IMFSampleProtection::GetProtectionCertificate


## -description

Retrieves the sample protection certificate.

## -parameters

### -param dwVersion [in]

Specifies the version number of the sample protection scheme for which to receive a certificate. The version number is specified as a <a href="/windows/desktop/api/mfidl/ne-mfidl-sample_protection_version">SAMPLE_PROTECTION_VERSION</a> enumeration value.

### -param ppCert [out]

Receives a pointer to a buffer containing the certificate. The caller must free the memory for the buffer by calling <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a>.

### -param pcbCert [out]

Receives the size of the <i>ppCert</i> buffer, in bytes.

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

For certain version numbers of sample protection, the downstream component must provide a certificate. Components that do not support these version numbers can return E_NOTIMPL.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfsampleprotection">IMFSampleProtection</a>