---
UID: NF:msdrm.DRMConstructCertificateChain
title: DRMConstructCertificateChain function (msdrm.h)
description: Builds a certificate chain from an arbitrary number of certificates.
helpviewer_keywords: ["DRMConstructCertificateChain","DRMConstructCertificateChain function [Active Directory Rights Management Services SDK 1.0]","msdrm/DRMConstructCertificateChain","rm.drmconstructcertificatechain"]
old-location: rm\drmconstructcertificatechain.htm
tech.root: rm
ms.assetid: 27c2bf2e-54b1-4ed4-a754-e8b3b3bd58cb
ms.date: 12/05/2018
ms.keywords: DRMConstructCertificateChain, DRMConstructCertificateChain function [Active Directory Rights Management Services SDK 1.0], msdrm/DRMConstructCertificateChain, rm.drmconstructcertificatechain
req.header: msdrm.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Msdrm.lib
req.dll: Msdrm.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
req.product: Rights Management Services client 1.0 SP2 or later
ms.custom: 19H1
f1_keywords:
 - DRMConstructCertificateChain
 - msdrm/DRMConstructCertificateChain
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Msdrm.dll
api_name:
 - DRMConstructCertificateChain
---

# DRMConstructCertificateChain function


## -description

<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="/previous-versions/windows/desktop/msipc/microsoft-information-protection-and-control-client-portal">Active Directory Rights Management Services SDK 2.1</a>, 

which leverages functionality exposed by the client in Msipc.dll.]

The <b>DRMConstructCertificateChain</b> function builds a certificate chain from an arbitrary number of certificates.

## -parameters

### -param cCertificates [in]

The number of certificates in the <i>rgwszCertificates</i> array.

### -param rgwszCertificates [in]

An array of null-terminated Unicode string pointers that contain the certificates to construct the chain from. The number of elements in this array is specified by the <i>cCertificates</i> parameter.

### -param pcChain [in, out]

A pointer to a <b>UINT</b> that, on input, contains the size, in Unicode characters, of the  <i>wszChain</i> string. This character count must include the terminating null character.

On output, this <b>UINT</b> receives the number of Unicode characters copied into the buffer, including the terminating null character.

### -param wszChain [out]

A pointer to a null-terminated Unicode string that receives the constructed chain.

To determine the required size for this buffer, call this function with <b>NULL</b> for the <i>wszChain</i> parameter. The required number of Unicode characters, including the terminating null character, will be returned in the <i>pcChain</i> parameter.

## -returns

If the function succeeds, the function returns S_OK.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following list. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

Memory allocation and deallocation for the chain are handled by the caller. To determine the required size for the <i>wszChain</i> buffer, call this function with <b>NULL</b> for the <i>wszChain</i> parameter. The required number of Unicode characters, including the terminating null character, will be returned in the <i>pcChain</i> parameter.

This function can be used to transform certificate chains that are returned by the AD RMS SOAP methods into certificate chains that can be used by AD RMS functions. For an example, see <a href="/previous-versions/windows/desktop/adrms_sdk/decryption-getboundlicense-cpp">Decryption_GetBoundLicense.cpp</a>.

## -see-also

<a href="/previous-versions/windows/desktop/adrms_sdk/ad-rms-functions">AD RMS Functions</a>



<a href="/previous-versions/windows/desktop/adrms_sdk/decryption-getboundlicense-cpp">Decryption_GetBoundLicense.cpp</a>