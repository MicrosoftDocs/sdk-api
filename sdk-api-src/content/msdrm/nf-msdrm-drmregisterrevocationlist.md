---
UID: NF:msdrm.DRMRegisterRevocationList
title: DRMRegisterRevocationList function (msdrm.h)
description: Registers a rights revocation list on the client.
helpviewer_keywords: ["DRMRegisterRevocationList","DRMRegisterRevocationList function [Active Directory Rights Management Services SDK 1.0]","msdrm/DRMRegisterRevocationList","rm.drmregisterrevocationlist"]
old-location: rm\drmregisterrevocationlist.htm
tech.root: rm
ms.assetid: 819a8471-e447-4a4d-ae52-5929350df2c8
ms.date: 12/05/2018
ms.keywords: DRMRegisterRevocationList, DRMRegisterRevocationList function [Active Directory Rights Management Services SDK 1.0], msdrm/DRMRegisterRevocationList, rm.drmregisterrevocationlist
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
 - DRMRegisterRevocationList
 - msdrm/DRMRegisterRevocationList
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
 - DRMRegisterRevocationList
---

# DRMRegisterRevocationList function


## -description

<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="/previous-versions/windows/desktop/msipc/microsoft-information-protection-and-control-client-portal">Active Directory Rights Management Services SDK 2.1</a>, 

which leverages functionality exposed by the client in Msipc.dll.]

The <b>DRMRegisterRevocationList</b> function registers a rights revocation list on the client.

## -parameters

### -param hEnv [in]

A handle to an environment, created by <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drminitenvironment">DRMInitEnvironment</a>.

### -param wszRevocationList [in]

Revocation list as a null-terminated string.

## -returns

If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

A revocation list holds all group identities, end-user licenses, or other principals that have been revoked. This function blocks the display of content from distributors or users whose license has been revoked. When an attempt to bind to a license fails with <b>E_DRM_BIND_REVOCATION_LIST_STALE</b> or <b>E_DRM_BIND_NO_APPLICABLE_REVOCATION_LIST</b>, this indicates that the license requires a revocation list. This list must either be found in the license store (using <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmenumeratelicense">DRMEnumerateLicense</a>) or must be acquired fresh using <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmacquireadvisories">DRMAcquireAdvisories</a> and then retrieved from the license store. Registration is only for the lifetime of the environment passed in. Any time that a new environment object is created, the necessary revocation lists must be registered for that environment.

## -see-also

<a href="/previous-versions/windows/desktop/adrms_sdk/ad-rms-functions">AD RMS Functions</a>



<a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmacquireadvisories">DRMAcquireAdvisories</a>



<a href="/previous-versions/windows/desktop/adrms_sdk/revoking-a-certificate">Revoking a Certificate</a>