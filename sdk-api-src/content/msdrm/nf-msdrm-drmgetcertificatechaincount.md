---
UID: NF:msdrm.DRMGetCertificateChainCount
title: DRMGetCertificateChainCount function (msdrm.h)
description: Retrieves the number of certificates in a certificate chain.
helpviewer_keywords: ["DRMGetCertificateChainCount","DRMGetCertificateChainCount function [Active Directory Rights Management Services SDK 1.0]","msdrm/DRMGetCertificateChainCount","rm.drmgetcertificatechaincount"]
old-location: rm\drmgetcertificatechaincount.htm
tech.root: rm
ms.assetid: c19e7cfe-2a28-41d5-9075-3e159be1d9ab
ms.date: 12/05/2018
ms.keywords: DRMGetCertificateChainCount, DRMGetCertificateChainCount function [Active Directory Rights Management Services SDK 1.0], msdrm/DRMGetCertificateChainCount, rm.drmgetcertificatechaincount
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
 - DRMGetCertificateChainCount
 - msdrm/DRMGetCertificateChainCount
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
 - DRMGetCertificateChainCount
---

# DRMGetCertificateChainCount function


## -description

<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="/previous-versions/windows/desktop/msipc/microsoft-information-protection-and-control-client-portal">Active Directory Rights Management Services SDK 2.1</a>, 

which leverages functionality exposed by the client in Msipc.dll.]

The <b>DRMGetCertificateChainCount</b> function retrieves the number of certificates in a certificate chain.

## -parameters

### -param wszChain [in]

The chain to count.

### -param pcCertCount [out]

The number of certificates in the chain.

## -returns

If the function succeeds, the function returns S_OK.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following list. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

This function is used with <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmdeconstructcertificatechain">DRMDeconstructCertificateChain</a> to allow an application to loop through a certificate chain and retrieve individual certificates.

## -see-also

<a href="/previous-versions/windows/desktop/adrms_sdk/ad-rms-functions">AD RMS Functions</a>