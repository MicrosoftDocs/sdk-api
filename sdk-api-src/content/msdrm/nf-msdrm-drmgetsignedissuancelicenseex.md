---
UID: NF:msdrm.DRMGetSignedIssuanceLicenseEx
title: DRMGetSignedIssuanceLicenseEx function (msdrm.h)
author: windows-sdk-content
description: Acquires a signed issuance license offline.
old-location: rm\drmgetsignedissuancelicenseex.htm
tech.root: AdRms_Sdk
ms.assetid: 9d37f69e-e582-4efc-9f17-866f195e439a
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DRMGetSignedIssuanceLicenseEx, DRMGetSignedIssuanceLicenseEx function [Active Directory Rights Management Services SDK 1.0], DRM_AUTO_GENERATE_KEY, DRM_OWNER_LICENSE_NOPERSIST, DRM_REUSE_KEY, DRM_SIGN_CANCEL, DRM_SIGN_OFFLINE, msdrm/DRMGetSignedIssuanceLicenseEx, rm.drmgetsignedissuancelicenseex
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Msdrm.dll
api_name:
 - DRMGetSignedIssuanceLicenseEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DRMGetSignedIssuanceLicenseEx function


## -description


<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/a7900f40-4c53-4760-8e5a-9c88149f86d0">Active Directory Rights Management Services SDK 2.1</a>, 

which leverages functionality exposed by the client in Msipc.dll.]

The <b>DRMGetSignedIssuanceLicenseEx</b> function  acquires a signed issuance license offline. When you call the function, you can pass in  the handle to a client licensor certificate (CLC) and the handle to a rights account certificate (RAC), therefore specifying the CLC and the RAC to use when acquiring the signed issuance license.


## -parameters




### -param hEnv [in]

A handle to a secure environment created by using the <a href="https://msdn.microsoft.com/b46277f4-e854-4590-847a-cf4f878bee70">DRMInitEnvironment</a> function. The handle is required for offline signing. Applications that do not use a lockbox should pass <b>NULL</b> for this parameter.


### -param hIssuanceLicense [in]

A handle to an issuance license to sign, created by using the <a href="https://msdn.microsoft.com/db2e9aa6-7021-4805-8fd7-94c8d02776b0">DRMCreateIssuanceLicense</a> function.


### -param uFlags [in]

Contains various options for acquiring the signed issuance license. This parameter can be one of the following values (although <b>DRM_AUTO_GENERATE_KEY</b> and <b>DRM_OWNER_LICENSE_NOPERSIST</b> can be combined with other flags). If <b>DRM_AUTO_GENERATE_KEY</b> is not specified, you must provide your own content key with a cryptographic system, such as the CryptoAPI functions from the Platform SDK.



#### DRM_SIGN_OFFLINE

Specifies an offline issuance license signing request. When signing offline, the issuance license is signed by using the <a href="https://msdn.microsoft.com/en-us/library/Aa362374(v=VS.85).aspx">client licensor certificate</a> (CLC) obtained during a previous call to <a href="https://msdn.microsoft.com/0d4ce794-8384-4f1c-bc8c-1e67fbb5f987">DRMAcquireLicense</a>. To get this certificate from the store, use <a href="https://msdn.microsoft.com/7a7797f2-d219-4a17-ac3d-96134cd14a55">DRMEnumerateLicense</a>. Each CLC is tied to the server that issued it; be sure that you are using the correct client licensor certificate for the issuance license you are publishing.

This flag cannot be combined with the <b>DRM_SIGN_ONLINE</b> or <b>DRM_SERVER_ISSUANCELICENSE</b> flags.



#### DRM_SIGN_CANCEL

Cancels an online signing request. Offline requests are processed immediately and do not need to be canceled.



#### DRM_AUTO_GENERATE_KEY

Can be used with one of the preceding flags to have the Active Directory Rights Management Services system generate a content key for you. This key is used in encryption functions. Typically, the key type  is AES and the cipher mode is ECB. If this flag is not specified, you must provide your own content key with a cryptographic system, such as with the CryptoAPI functions from the Platform SDK.

<div class="alert"><b>Note</b>  If you are using the AD RMS client included in  Windows 7,  or if you install the <a href="http://go.microsoft.com/fwlink/p/?linkid=155817">CBC hotfix</a>, the value AES_CBC4K can be used to specify the AES algorithm with cipher-block chaining (CBC) cipher mode. See the <a href="https://msdn.microsoft.com/1de19409-2b14-4ab0-9853-23ee5741a7ae">DRMEncrypt</a> code examples for more information.</div>
<div> </div>


#### DRM_OWNER_LICENSE_NOPERSIST

The owner license is stored in memory instead of the permanent store. The owner license can subsequently be retrieved by the <a href="https://msdn.microsoft.com/e657ac08-9635-40ac-8d9f-cc8ab9ed3a6c">DRMGetOwnerLicense</a> function.



#### DRM_REUSE_KEY

Causes the content key to be reused. The content key is obtained from the signed issuance license associated with the bound license (<i>hBoundLicense</i>) that is passed in to <a href="https://msdn.microsoft.com/db2e9aa6-7021-4805-8fd7-94c8d02776b0">DRMCreateIssuanceLicense</a>. You must ensure that the bound license is bound to either the <b>EDITRIGHTSDATA</b> or <b>OWNER</b> right. This flag is available only in  Windows 7.

<div class="alert"><b>Note</b>  This flag must be combined with <b>DRM_SIGN_OFFLINE</b>. You can also optionally combine it with <b>DRM_OWNER_LICENSE_NOPERSIST</b>. These are the only allowed values. The parameters <i>pbSymKey</i> and <i>cbSymKey</i> must be set to 0.</div>
<div> </div>
<div class="alert"><b>Caution</b>  To avoid security implications, reuse the content key only if users or rights are being added. Additionally, it is a best practice to always generate a new content identifier for the publishing license to avoid an older end-user license being used with the new publishing license.</div>
<div> </div>

### -param pbSymKey [in]

The content key used to encrypt the document. If this value is <b>NULL</b>, the <i>uFlags</i> parameter must specify <b>DRM_AUTO_GENERATE_KEY</b> or <b>DRM_REUSE_KEY</b>. These <i>uFlags</i> values cause <i>pbSymKey</i> to be ignored.


### -param cbSymKey [in]

The size, in bytes, of the content key. Currently, this parameter can only be 16 unless the <i>uFlags</i> parameter specifies <b>DRM_AUTO_GENERATE_KEY</b> or <b>DRM_REUSE_KEY</b>, in which case this parameter can be zero.


### -param wszSymKeyType [in]

The key type. The value <b>AES</b> specifies the Advanced Encryption Standard (AES) algorithm with the  electronic code book (ECB) cipher mode. If you are using Windows 7, the value <b>AES_CBC4K</b> can be used to specify the AES algorithm with cipher-block chaining (CBC) cipher mode. See the <a href="https://msdn.microsoft.com/1de19409-2b14-4ab0-9853-23ee5741a7ae">DRMEncrypt</a> code examples for more information.


### -param pvReserved [in]

Reserved for future use.


### -param hEnablingPrincipal [in]

A handle to an enabling principal in the end-user license that should be bound. Create this handle by using the <a href="https://msdn.microsoft.com/92858a46-cef5-4d25-9f3c-cbb343743565">DRMCreateEnablingPrincipal</a> function by passing in the rights account certificate. This parameter is required.


### -param hBoundLicenseCLC [in]

A handle to the bound license corresponding to the client licensor certificate created using <a href="https://msdn.microsoft.com/102fa347-47be-4dc7-ba17-3f1ad3735b00">DRMCreateBoundLicense</a>. This can be created by binding the <i>wszClientLicensorCertificate</i> to the <b>ISSUE</b> right using the <i>hEnablingPrincipal</i> handle. This parameter is required.


### -param pfnCallback [in]

A pointer to the callback function used to notify the application of an asynchronous request's progress. For the signature of the callback function you must provide, see <a href="https://msdn.microsoft.com/41c200df-afbc-43a5-8046-d131fec3261a">Callback Prototype</a>.


### -param pvContext [in]

A 32-bit, application-defined value that is sent in the <i>pvContext</i> parameter of the callback function. This value can be a pointer to data, a pointer to an event handle, or whatever else the custom callback function is designed to handle. For more information, see <a href="https://msdn.microsoft.com/7d880b74-1934-4282-a7ca-1dac3602d6b4">Creating a Callback Function</a>.


## -returns



If the function succeeds, the function returns S_OK.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following list. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



To use this function, create an enabling principal from the rights account certificate using <a href="https://msdn.microsoft.com/92858a46-cef5-4d25-9f3c-cbb343743565">DRMCreateEnablingPrincipal</a>. After this, you must parse the client licensor certificate(CLC) to obtain the content ID, in the same manner as you do for the end-user license. Subsequently, call <a href="https://msdn.microsoft.com/102fa347-47be-4dc7-ba17-3f1ad3735b00">DRMCreateBoundLicense</a>, passing in the <i>hEnablingPrincipal</i> obtained from the call to <b>DRMCreateEnablingPrincipal</b> and the content ID to create an <i>hBoundLicense</i> that corresponds with the CLC. Next, call <b>DRMGetSignedIssuanceLicenseEx</b>, passing in the <i>hEnablingPrincipal</i> obtained from the call to <b>DRMCreateEnablingPrincipal</b> and the <i>hBoundLicense</i> obtained from the call to <b>DRMCreateBoundLicense</b>. Finally, cache the handles obtained from the call to <b>DRMCreateEnablingPrincipal</b> and the call to <b>DRMCreateBoundLicense</b>.




## -see-also




<a href="https://msdn.microsoft.com/b3b4e7c6-d3d3-4bf7-b6c4-9502a56a7223">AD RMS Functions</a>



<a href="https://msdn.microsoft.com/9948c2a4-cb42-42c1-bd22-33d39c039391">Creating and Using Issuance Licenses</a>



<a href="https://msdn.microsoft.com/a156994b-e6a8-42dc-8a49-cae20ea2e9da">Offline Signing Code Example</a>



<a href="https://msdn.microsoft.com/93b509a5-4997-46cd-823f-5529ec966ac6">Online Signing Code Example</a>
 

 

