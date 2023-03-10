---
UID: NF:msdrm.DRMGetSignedIssuanceLicenseEx
title: DRMGetSignedIssuanceLicenseEx function (msdrm.h)
description: Acquires a signed issuance license offline.
helpviewer_keywords: ["DRMGetSignedIssuanceLicenseEx","DRMGetSignedIssuanceLicenseEx function [Active Directory Rights Management Services SDK 1.0]","DRM_AUTO_GENERATE_KEY","DRM_OWNER_LICENSE_NOPERSIST","DRM_REUSE_KEY","DRM_SIGN_CANCEL","DRM_SIGN_OFFLINE","msdrm/DRMGetSignedIssuanceLicenseEx","rm.drmgetsignedissuancelicenseex"]
old-location: rm\drmgetsignedissuancelicenseex.htm
tech.root: rm
ms.assetid: 9d37f69e-e582-4efc-9f17-866f195e439a
ms.date: 12/05/2018
ms.keywords: DRMGetSignedIssuanceLicenseEx, DRMGetSignedIssuanceLicenseEx function [Active Directory Rights Management Services SDK 1.0], DRM_AUTO_GENERATE_KEY, DRM_OWNER_LICENSE_NOPERSIST, DRM_REUSE_KEY, DRM_SIGN_CANCEL, DRM_SIGN_OFFLINE, msdrm/DRMGetSignedIssuanceLicenseEx, rm.drmgetsignedissuancelicenseex
req.header: msdrm.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7
req.target-min-winversvr: Windows Server 2008 R2
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
ms.custom: 19H1
f1_keywords:
 - DRMGetSignedIssuanceLicenseEx
 - msdrm/DRMGetSignedIssuanceLicenseEx
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
 - DRMGetSignedIssuanceLicenseEx
---

# DRMGetSignedIssuanceLicenseEx function


## -description

<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="/previous-versions/windows/desktop/msipc/microsoft-information-protection-and-control-client-portal">Active Directory Rights Management Services SDK 2.1</a>, 

which leverages functionality exposed by the client in Msipc.dll.]

The <b>DRMGetSignedIssuanceLicenseEx</b> function  acquires a signed issuance license offline. When you call the function, you can pass in  the handle to a client licensor certificate (CLC) and the handle to a rights account certificate (RAC), therefore specifying the CLC and the RAC to use when acquiring the signed issuance license.

## -parameters

### -param hEnv [in]

A handle to a secure environment created by using the <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drminitenvironment">DRMInitEnvironment</a> function. The handle is required for offline signing. Applications that do not use a lockbox should pass <b>NULL</b> for this parameter.

### -param hIssuanceLicense [in]

A handle to an issuance license to sign, created by using the <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmcreateissuancelicense">DRMCreateIssuanceLicense</a> function.

### -param uFlags [in]

Contains various options for acquiring the signed issuance license. This parameter can be one of the following values (although <b>DRM_AUTO_GENERATE_KEY</b> and <b>DRM_OWNER_LICENSE_NOPERSIST</b> can be combined with other flags). If <b>DRM_AUTO_GENERATE_KEY</b> is not specified, you must provide your own content key with a cryptographic system, such as the CryptoAPI functions from the Platform SDK.



#### DRM_SIGN_OFFLINE

Specifies an offline issuance license signing request. When signing offline, the issuance license is signed by using the <a href="/previous-versions/windows/desktop/adrms_sdk/c-gly">client licensor certificate</a> (CLC) obtained during a previous call to <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmacquirelicense">DRMAcquireLicense</a>. To get this certificate from the store, use <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmenumeratelicense">DRMEnumerateLicense</a>. Each CLC is tied to the server that issued it; be sure that you are using the correct client licensor certificate for the issuance license you are publishing.

This flag cannot be combined with the <b>DRM_SIGN_ONLINE</b> or <b>DRM_SERVER_ISSUANCELICENSE</b> flags.



#### DRM_SIGN_CANCEL

Cancels an online signing request. Offline requests are processed immediately and do not need to be canceled.



#### DRM_AUTO_GENERATE_KEY

Can be used with one of the preceding flags to have the Active Directory Rights Management Services system generate a content key for you. This key is used in encryption functions. Typically, the key type  is AES and the cipher mode is ECB. If this flag is not specified, you must provide your own content key with a cryptographic system, such as with the CryptoAPI functions from the Platform SDK.

<div class="alert"><b>Note</b>  If you are using the AD RMS client included in  Windows 7,  or if you install the CBC hotfix, the value AES_CBC4K can be used to specify the AES algorithm with cipher-block chaining (CBC) cipher mode. See the <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmencrypt">DRMEncrypt</a> code examples for more information.</div>
<div> </div>


#### DRM_OWNER_LICENSE_NOPERSIST

The owner license is stored in memory instead of the permanent store. The owner license can subsequently be retrieved by the <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmgetownerlicense">DRMGetOwnerLicense</a> function.



#### DRM_REUSE_KEY

Causes the content key to be reused. The content key is obtained from the signed issuance license associated with the bound license (<i>hBoundLicense</i>) that is passed in to <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmcreateissuancelicense">DRMCreateIssuanceLicense</a>. You must ensure that the bound license is bound to either the <b>EDITRIGHTSDATA</b> or <b>OWNER</b> right. This flag is available only in  Windows 7.

<div class="alert"><b>Note</b>  This flag must be combined with <b>DRM_SIGN_OFFLINE</b>. You can also optionally combine it with <b>DRM_OWNER_LICENSE_NOPERSIST</b>. These are the only allowed values. The parameters <i>pbSymKey</i> and <i>cbSymKey</i> must be set to 0.</div>
<div> </div>
<div class="alert"><b>Caution</b>  To avoid security implications, reuse the content key only if users or rights are being added. Additionally, it is a best practice to always generate a new content identifier for the publishing license to avoid an older end-user license being used with the new publishing license.</div>
<div> </div>

### -param pbSymKey [in]

The content key used to encrypt the document. If this value is <b>NULL</b>, the <i>uFlags</i> parameter must specify <b>DRM_AUTO_GENERATE_KEY</b> or <b>DRM_REUSE_KEY</b>. These <i>uFlags</i> values cause <i>pbSymKey</i> to be ignored.

### -param cbSymKey [in]

The size, in bytes, of the content key. Currently, this parameter can only be 16 unless the <i>uFlags</i> parameter specifies <b>DRM_AUTO_GENERATE_KEY</b> or <b>DRM_REUSE_KEY</b>, in which case this parameter can be zero.

### -param wszSymKeyType [in]

The key type. The value <b>AES</b> specifies the Advanced Encryption Standard (AES) algorithm with the  electronic code book (ECB) cipher mode. If you are using Windows 7, the value <b>AES_CBC4K</b> can be used to specify the AES algorithm with cipher-block chaining (CBC) cipher mode. See the <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmencrypt">DRMEncrypt</a> code examples for more information.

### -param pvReserved [in]

Reserved for future use.

### -param hEnablingPrincipal [in]

A handle to an enabling principal in the end-user license that should be bound. Create this handle by using the <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmcreateenablingprincipal">DRMCreateEnablingPrincipal</a> function by passing in the rights account certificate. This parameter is required.

### -param hBoundLicenseCLC [in]

A handle to the bound license corresponding to the client licensor certificate created using <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmcreateboundlicense">DRMCreateBoundLicense</a>. This can be created by binding the <i>wszClientLicensorCertificate</i> to the <b>ISSUE</b> right using the <i>hEnablingPrincipal</i> handle. This parameter is required.

### -param pfnCallback [in]

A pointer to the callback function used to notify the application of an asynchronous request's progress. For the signature of the callback function you must provide, see <a href="/previous-versions/windows/desktop/api/msdrmdefs/nc-msdrmdefs-drmcallback">Callback Prototype</a>.

### -param pvContext [in]

A 32-bit, application-defined value that is sent in the <i>pvContext</i> parameter of the callback function. This value can be a pointer to data, a pointer to an event handle, or whatever else the custom callback function is designed to handle. For more information, see <a href="/previous-versions/windows/desktop/adrms_sdk/creating-a-callback-function">Creating a Callback Function</a>.

## -returns

If the function succeeds, the function returns S_OK.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following list. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

To use this function, create an enabling principal from the rights account certificate using <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmcreateenablingprincipal">DRMCreateEnablingPrincipal</a>. After this, you must parse the client licensor certificate(CLC) to obtain the content ID, in the same manner as you do for the end-user license. Subsequently, call <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmcreateboundlicense">DRMCreateBoundLicense</a>, passing in the <i>hEnablingPrincipal</i> obtained from the call to <b>DRMCreateEnablingPrincipal</b> and the content ID to create an <i>hBoundLicense</i> that corresponds with the CLC. Next, call <b>DRMGetSignedIssuanceLicenseEx</b>, passing in the <i>hEnablingPrincipal</i> obtained from the call to <b>DRMCreateEnablingPrincipal</b> and the <i>hBoundLicense</i> obtained from the call to <b>DRMCreateBoundLicense</b>. Finally, cache the handles obtained from the call to <b>DRMCreateEnablingPrincipal</b> and the call to <b>DRMCreateBoundLicense</b>.

## -see-also

<a href="/previous-versions/windows/desktop/adrms_sdk/ad-rms-functions">AD RMS Functions</a>



<a href="/previous-versions/windows/desktop/adrms_sdk/creating-and-using-issuance-licenses">Creating and Using Issuance Licenses</a>



<a href="/previous-versions/windows/desktop/adrms_sdk/offline-signing-code-example">Offline Signing Code Example</a>



<a href="/previous-versions/windows/desktop/adrms_sdk/online-signing-code-example">Online Signing Code Example</a>