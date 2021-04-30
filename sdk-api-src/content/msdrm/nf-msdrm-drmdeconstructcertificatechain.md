---
UID: NF:msdrm.DRMDeconstructCertificateChain
title: DRMDeconstructCertificateChain function (msdrm.h)
description: Retrieves a specified certificate from a certificate chain.
helpviewer_keywords: ["DRMDeconstructCertificateChain","DRMDeconstructCertificateChain function [Active Directory Rights Management Services SDK 1.0]","msdrm/DRMDeconstructCertificateChain","rm.drmdeconstructcertificatechain"]
old-location: rm\drmdeconstructcertificatechain.htm
tech.root: rm
ms.assetid: 893263cc-2647-4f62-b997-354ea976081f
ms.date: 12/05/2018
ms.keywords: DRMDeconstructCertificateChain, DRMDeconstructCertificateChain function [Active Directory Rights Management Services SDK 1.0], msdrm/DRMDeconstructCertificateChain, rm.drmdeconstructcertificatechain
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
 - DRMDeconstructCertificateChain
 - msdrm/DRMDeconstructCertificateChain
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
 - DRMDeconstructCertificateChain
---

# DRMDeconstructCertificateChain function


## -description

<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="/previous-versions/windows/desktop/msipc/microsoft-information-protection-and-control-client-portal">Active Directory Rights Management Services SDK 2.1</a>, 

which leverages functionality exposed by the client in Msipc.dll.]

The <b>DRMDeconstructCertificateChain</b> function retrieves a specified certificate from a certificate chain.

## -parameters

### -param wszChain [in]

The certificate chain.

### -param iWhich [in]

A zero-based index specifying which certificate to retrieve.

### -param pcCert [in, out]

The length of the retrieved certificate, in characters, plus one for a null terminator.

### -param wszCert [out]

The certificate requested.

## -returns

If the function succeeds, the function returns S_OK.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following list. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

This function allows an application to retrieve individual certificates from a chain. To determine the number of certificates available, use <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmgetcertificatechaincount">DRMGetCertificateChainCount</a>.

Memory allocation and deallocation for <i>wszCert</i> are handled by the caller. The <i>szChain</i> buffer length can be obtained from the <i>pcCert</i> parameter by calling this function with <b>NULL</b> in the <i>wszCert</i> parameter.

## -see-also

<a href="/previous-versions/windows/desktop/adrms_sdk/ad-rms-functions">AD RMS Functions</a>



<a href="/previous-versions/windows/desktop/adrms_sdk/decryption-getboundlicense-cpp">Decryption_GetBoundLicense.cpp</a>