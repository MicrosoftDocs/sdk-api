---
UID: NF:msdrm.DRMCreateLicenseStorageSession
title: DRMCreateLicenseStorageSession function (msdrm.h)
description: Creates a license storage session, which is needed to acquire or manipulate a license.
helpviewer_keywords: ["DRMCreateLicenseStorageSession","DRMCreateLicenseStorageSession function [Active Directory Rights Management Services SDK 1.0]","msdrm/DRMCreateLicenseStorageSession","rm.drmcreatelicensestoragesession"]
old-location: rm\drmcreatelicensestoragesession.htm
tech.root: rm
ms.assetid: 6561b6df-373b-4bd3-9196-09ef945f8042
ms.date: 12/05/2018
ms.keywords: DRMCreateLicenseStorageSession, DRMCreateLicenseStorageSession function [Active Directory Rights Management Services SDK 1.0], msdrm/DRMCreateLicenseStorageSession, rm.drmcreatelicensestoragesession
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
 - DRMCreateLicenseStorageSession
 - msdrm/DRMCreateLicenseStorageSession
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
 - DRMCreateLicenseStorageSession
---

# DRMCreateLicenseStorageSession function


## -description

<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="/previous-versions/windows/desktop/msipc/microsoft-information-protection-and-control-client-portal">Active Directory Rights Management Services SDK 2.1</a>, 

which leverages functionality exposed by the client in Msipc.dll.]

The <b>DRMCreateLicenseStorageSession</b> function creates a license storage session, which is needed to acquire or manipulate a license.

## -parameters

### -param hEnv [in]

A handle to the AD RMS environment. This handle is obtained by using the <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drminitenvironment">DRMInitEnvironment</a> function.

### -param hDefaultLibrary [in]

A handle to the default library. This handle is obtained by using the <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drminitenvironment">DRMInitEnvironment</a> function.

### -param hClient [in]

A handle to a client session. This handle is obtained by using the <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmcreateclientsession">DRMCreateClientSession</a> function.

### -param uFlags [in]

This parameter is reserved and must be set to zero.

### -param wszIssuanceLicense [in]

A pointer to a null-terminated Unicode string that contains a signed issuance license. The created license storage session is associated with this issuance license.

### -param phLicenseStorage [out]

A pointer to a handle that receives the license storage session handle. This handle must be passed to the <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmclosesession">DRMCloseSession</a> function when the license storage session is no longer needed.

## -returns

 If the function succeeds, the function returns S_OK.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

A license storage session is used for acquiring, deleting, and enumerating licenses, among other uses. To actually bind to a license and exercise its rights, an application must use <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmcreateboundlicense">DRMCreateBoundLicense</a>.

The environment handle and default library handle are created by using <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drminitenvironment">DRMInitEnvironment</a>.

The handle returned in the <i>phLicenseStorage</i> parameter must be passed to the <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmclosesession">DRMCloseSession</a> function when the license storage session is no longer needed.

## -see-also

<a href="/previous-versions/windows/desktop/adrms_sdk/ad-rms-functions">AD RMS Functions</a>



<a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmclosehandle">DRMCloseHandle</a>



<a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmcreateclientsession">DRMCreateClientSession</a>



<a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drminitenvironment">DRMInitEnvironment</a>



<a href="/previous-versions/windows/desktop/adrms_sdk/decryption-getboundlicense-cpp">Decryption_GetBoundLicense.cpp</a>