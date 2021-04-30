---
UID: NF:msdrm.DRMCreateBoundLicense
title: DRMCreateBoundLicense function (msdrm.h)
description: Allows an application to examine or exercise the rights on a locally stored license.
helpviewer_keywords: ["DRMCreateBoundLicense","DRMCreateBoundLicense function [Active Directory Rights Management Services SDK 1.0]","msdrm/DRMCreateBoundLicense","rm.drmcreateboundlicense"]
old-location: rm\drmcreateboundlicense.htm
tech.root: rm
ms.assetid: 102fa347-47be-4dc7-ba17-3f1ad3735b00
ms.date: 12/05/2018
ms.keywords: DRMCreateBoundLicense, DRMCreateBoundLicense function [Active Directory Rights Management Services SDK 1.0], msdrm/DRMCreateBoundLicense, rm.drmcreateboundlicense
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
 - DRMCreateBoundLicense
 - msdrm/DRMCreateBoundLicense
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
 - DRMCreateBoundLicense
---

# DRMCreateBoundLicense function


## -description

<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="/previous-versions/windows/desktop/msipc/microsoft-information-protection-and-control-client-portal">Active Directory Rights Management Services SDK 2.1</a>, 

which leverages functionality exposed by the client in Msipc.dll.]

The <b>DRMCreateBoundLicense</b> function allows an application to examine or exercise the rights on a locally stored license.

## -parameters

### -param hEnv [in]

A handle to an environment; the handle is created by using the <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drminitenvironment">DRMInitEnvironment</a> function.

### -param pParams [in]

A pointer to a <a href="/windows/desktop/api/msdrmdefs/ns-msdrmdefs-drmboundlicenseparams">DRMBOUNDLICENSEPARAMS</a> structure that specifies additional options; for more information, see the Remarks section. The principal specified here is the one the application will try to bind to. If you pass in <b>NULL</b> to identify the principal or rights group, the first principal or rights group in the license will be used.

### -param wszLicenseChain [in]

A pointer to a null-terminated Unicode string that contains the <a href="/previous-versions/windows/desktop/adrms_sdk/e-gly">end-user license</a> (or license chain).

### -param phBoundLicense [out]

A pointer to a handle that receives the bound license. The <b>DRMHANDLE</b> passed back through <i>phBoundLicense</i> allows an application to navigate through all the license's objects (such as principals or rights) and attributes (such as maximum play count). A bound license consolidates duplicated rights information in the license and removes any rights information that is not available to the current user.

### -param phErrorLog [out]

This parameter must be <b>NULL</b>.

## -returns

If the function succeeds, the function returns S_OK.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following list. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

Calling this function binds a license to the right or rights specified in the  <a href="/windows/desktop/api/msdrmdefs/ns-msdrmdefs-drmboundlicenseparams">DRMBOUNDLICENSEPARAMS</a> structure passed to the <i>pParams</i> parameter. If any right requested cannot be exercised by the current user, the function will fail. Note also that you must call <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmsetmetadata">DRMSetMetaData</a> and specify a value for the <i>wszContentId</i> parameter before calling this function and that this value must be the same as the ID set in the <b>DRMBOUNDLICENSEPARAMS</b> structure or the function will fail.

If the function succeeds, it returns a handle to the bound license that can be examined, and also allows an application to exercise the bound right. This function does not decrement metered rights. Decrementing metered rights upon use is the responsibility of the application.

When license binding fails because of a missing or out of date revocation list, the return value does not indicate which license or certificate is causing the error. It could be the end-user license, the user's <a href="/previous-versions/windows/desktop/adrms_sdk/r-gly">rights account certificate</a>, a <a href="/previous-versions/windows/desktop/adrms_sdk/c-gly">client licensor certificate</a>, or another license or certificate. You must call <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmacquireadvisories">DRMAcquireAdvisories</a> (and <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmregisterrevocationlist">DRMRegisterRevocationList</a>) for each certificate until the error does not occur.

Principal authenticators required for a license must be loaded before calling this function. However, the authenticator can continue to function after the license is created.

When you have finished using the license handle, close it by calling the <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmclosehandle">DRMCloseHandle</a> function. <b>DRMCloseHandle</b> closes the handle to the library and deletes the license from memory.


The handle returned by this function can be passed into one of the following functions to navigate deeper into the license hierarchy:

<ul>
<li>
<a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmgetboundlicenseattribute">DRMGetBoundLicenseAttribute</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmgetboundlicenseattributecount">DRMGetBoundLicenseAttributeCount</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmgetboundlicenseobject">DRMGetBoundLicenseObject</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmgetboundlicenseobjectcount">DRMGetBoundLicenseObjectCount</a>
</li>
</ul>

## -see-also

<a href="/previous-versions/windows/desktop/adrms_sdk/ad-rms-functions">AD RMS Functions</a>



<a href="/windows/desktop/api/msdrmdefs/ns-msdrmdefs-drmboundlicenseparams">DRMBOUNDLICENSEPARAMS</a>