---
UID: NF:msdrm.DRMAcquireAdvisories
title: DRMAcquireAdvisories function (msdrm.h)
description: Retrieves revocation lists required by a submitted license.
helpviewer_keywords: ["DRMAcquireAdvisories","DRMAcquireAdvisories function [Active Directory Rights Management Services SDK 1.0]","msdrm/DRMAcquireAdvisories","rm.drmacquireadvisories"]
old-location: rm\drmacquireadvisories.htm
tech.root: rm
ms.assetid: 42c58096-429c-4278-b9ab-8c5a91361af8
ms.date: 12/05/2018
ms.keywords: DRMAcquireAdvisories, DRMAcquireAdvisories function [Active Directory Rights Management Services SDK 1.0], msdrm/DRMAcquireAdvisories, rm.drmacquireadvisories
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
 - DRMAcquireAdvisories
 - msdrm/DRMAcquireAdvisories
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
 - DRMAcquireAdvisories
---

# DRMAcquireAdvisories function


## -description

<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="/previous-versions/windows/desktop/msipc/microsoft-information-protection-and-control-client-portal">Active Directory Rights Management Services SDK 2.1</a>, 

which leverages functionality exposed by the client in Msipc.dll.]

The <b>DRMAcquireAdvisories</b> function retrieves revocation lists required by a submitted license. Retrieved revocation lists are added to the user's permanent license store. A revocation list is a signed XrML document that specifies principals that have been revoked because they are no longer considered trustworthy or valid. These principals can include <a href="/previous-versions/windows/desktop/adrms_sdk/r-gly">rights account certificates</a>, <a href="/previous-versions/windows/desktop/adrms_sdk/m-gly">machine certificates</a>, code-signing certificates, manifests, and server licensor certificates, among other things.

## -parameters

### -param hLicenseStorage [in]

A handle to a license storage session created by using the <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmcreatelicensestoragesession">DRMCreateLicenseStorageSession</a> function.

### -param wszLicense [in]

A pointer to a null-terminated Unicode string that contains the license that requires a revocation list. This can be any license or certificate (or certificate chain or concatenated licenses) that supports revocation lists, including <a href="/previous-versions/windows/desktop/adrms_sdk/e-gly">end-user licenses</a>, <a href="/previous-versions/windows/desktop/adrms_sdk/r-gly">rights account certificates</a>, or <a href="/previous-versions/windows/desktop/adrms_sdk/c-gly">client licensor certificates</a>.

### -param wszURL [in, optional]

A pointer to a null-terminated Unicode string that contains an additional URL to query for advisories. This will be checked in addition to any URLs mentioned in the license passed in. This parameter can be set to <b>NULL</b>.

### -param pvContext [in]

A 32-bit, application-defined value that is sent in the <i>pvContext</i> parameter of the callback function. This value can be a pointer to data, a pointer to an event handle, or whatever else the custom callback function is designed to handle. For more information, see <a href="/previous-versions/windows/desktop/api/msdrmdefs/nc-msdrmdefs-drmcallback">Callback Prototype</a>.

## -returns

If the function succeeds, the function returns S_OK.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

This function retrieves advisory lists asynchronously. The URL where the revocation list is posted is stored in the license that is passed in, but it can be overridden by <i>wszURL</i>.

After an advisory list has been obtained, it must be registered by using <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmregisterrevocationlist">DRMRegisterRevocationList</a>. It is simplest to enumerate all licenses in the license store by using <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmenumeratelicense">DRMEnumerateLicense</a> and then register each, rather than attempting to locate the item you just acquired.

You should periodically delete duplicate or outdated revocation lists from the license store by enumerating revocation lists. To enumerate revocation lists, call <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmenumeratelicense">DRMEnumerateLicense</a> with the <b>DRM_EL_EXPIRED</b> flag, and then call <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmdeletelicense">DRMDeleteLicense</a>. Because enumerating and examining licenses can be time-consuming, an application might perform this task only periodically.

An application will be informed that a new revocation list must be acquired if the call to the <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmcreateboundlicense">DRMCreateBoundLicense</a> function returns <b>E_DRM_BIND_REVOCATION_LIST_STALE</b> or <b>E_DRM_BIND_NO_APPLICABLE_REVOCATION_LIST</b>.

For more information about revocation lists and how to create them, see the Active Directory Rights Management Services deployment guide, which comes with <a href="/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831364(v=ws.11)">Rights Management Services</a>.

The application callback function specified in the <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmcreateclientsession">DRMCreateClientSession</a> function will be called with the <a href="/previous-versions/windows/desktop/adrms_sdk/drm-msg-acquire-advisory">DRM_MSG_ACQUIRE_ADVISORY</a> message to provide status feedback.

## -see-also

<a href="/previous-versions/windows/desktop/adrms_sdk/ad-rms-functions">AD RMS Functions</a>



<a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmregisterrevocationlist">DRMRegisterRevocationList</a>



<a href="/previous-versions/windows/desktop/adrms_sdk/revoking-a-certificate">Revoking a Certificate</a>