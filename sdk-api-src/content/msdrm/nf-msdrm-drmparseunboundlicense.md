---
UID: NF:msdrm.DRMParseUnboundLicense
title: DRMParseUnboundLicense function (msdrm.h)
description: Creates a handle to an unbound license, to allow an application to navigate its objects and attributes.
helpviewer_keywords: ["DRMParseUnboundLicense","DRMParseUnboundLicense function [Active Directory Rights Management Services SDK 1.0]","msdrm/DRMParseUnboundLicense","rm.drmparseunboundlicense"]
old-location: rm\drmparseunboundlicense.htm
tech.root: rm
ms.assetid: 2ae65ed2-7702-4e9b-b986-68b83ebe8bf5
ms.date: 12/05/2018
ms.keywords: DRMParseUnboundLicense, DRMParseUnboundLicense function [Active Directory Rights Management Services SDK 1.0], msdrm/DRMParseUnboundLicense, rm.drmparseunboundlicense
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
 - DRMParseUnboundLicense
 - msdrm/DRMParseUnboundLicense
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
 - DRMParseUnboundLicense
---

# DRMParseUnboundLicense function


## -description

<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="/previous-versions/windows/desktop/msipc/microsoft-information-protection-and-control-client-portal">Active Directory Rights Management Services SDK 2.1</a>, 

which leverages functionality exposed by the client in Msipc.dll.]

The <b>DRMParseUnboundLicense</b> function creates a handle to an unbound license, to allow an application to navigate its objects and attributes. For more information, see Remarks.

## -parameters

### -param wszCertificate [in]

The leaf certificate on the license to be examined, in plain text (not encoded).

### -param phQueryRoot [out]

Pointer to a handle to the root object of the license. Call <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmclosequeryhandle">DRMCloseQueryHandle</a> to close the handle.

## -returns

 If the function succeeds, the function returns S_OK.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

This function is for querying unbound end-user licenses, and also for obtaining license acquisition URLs from issuance licenses. The unbound end-user license retrieved by <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmenumeratelicense">DRMEnumerateLicense</a> is a certificate chain. To properly query the unbound license itself, first call <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmdeconstructcertificatechain">DRMDeconstructCertificateChain</a> to obtain the first element of the chain (item zero), which is the actual license.

An application can navigate this interface using various <b>DRMGetUnboundLicense_xxx</b> functions (for unbound licenses). To examine bound licenses, use the <b>DRMGetBoundLicense_xxx</b> functions.

Both bound and unbound licenses can be examined. Whether you decide to use a bound or an unbound license depends on whether you need to exercise the rights or just examine the license. Bound licenses can exist only after a secure environment has been created using <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drminitenvironment">DRMInitEnvironment</a>. Unbound licenses, however, do not require a secure environment.

The output of this function can be passed into one of the <b>DRMGetUnboundLicense_xxx</b> functions. The only object you can query for in an issuance license is g_wszQUERY_DISTRIBUTIONPOINT. The only attributes you can query for are g_wszQUERY_IDTYPE, g_wszQUERY_IDVALUE, g_wszQUERY_NAME, g_wszQUERY_ADDRESSTYPE, and g_wszQUERY_ADDRESSVALUE.

Call <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmclosequeryhandle">DRMCloseQueryHandle</a> to close the unbound license handle created by calling this function.

## -see-also

<a href="/previous-versions/windows/desktop/adrms_sdk/ad-rms-functions">AD RMS Functions</a>



<a href="/previous-versions/windows/desktop/adrms_sdk/querying-licenses">Querying Licenses</a>