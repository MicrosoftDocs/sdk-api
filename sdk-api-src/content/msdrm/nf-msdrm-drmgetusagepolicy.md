---
UID: NF:msdrm.DRMGetUsagePolicy
title: DRMGetUsagePolicy function (msdrm.h)
description: Gets a usage policy that requires, or denies, access to content based on application name, version, or other application characteristics.
helpviewer_keywords: ["DRMGetUsagePolicy","DRMGetUsagePolicy function [Active Directory Rights Management Services SDK 1.0]","msdrm/DRMGetUsagePolicy","rm.drmgetusagepolicy"]
old-location: rm\drmgetusagepolicy.htm
tech.root: rm
ms.assetid: 135ed2d0-17a9-46a2-9495-4102115f7bad
ms.date: 12/05/2018
ms.keywords: DRMGetUsagePolicy, DRMGetUsagePolicy function [Active Directory Rights Management Services SDK 1.0], msdrm/DRMGetUsagePolicy, rm.drmgetusagepolicy
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
 - DRMGetUsagePolicy
 - msdrm/DRMGetUsagePolicy
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
 - DRMGetUsagePolicy
---

# DRMGetUsagePolicy function


## -description

<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="/previous-versions/windows/desktop/msipc/microsoft-information-protection-and-control-client-portal">Active Directory Rights Management Services SDK 2.1</a>, 

which leverages functionality exposed by the client in Msipc.dll.]

The <b>DRMGetUsagePolicy</b> function gets a usage policy that requires, or denies, access to content based on application name, version, or other application characteristics.

## -parameters

### -param hIssuanceLicense [in]

The handle of the issuance license that the usage policy is contained in.

### -param uIndex [in]

The zero-based index of the policy to retrieve.

### -param peUsagePolicyType [out]

A pointer to a <a href="/windows/desktop/api/msdrmdefs/ne-msdrmdefs-drm_usagepolicy_type">DRM_USAGEPOLICY_TYPE</a> value that receives one of the <b>DRM_USAGEPOLICY_TYPE</b> values that specifies the type of usage policy (name, public key, and so on). If a usage policy of type <b>DRM_USAGEPOLICY_TYPE_BYNAME</b> is chosen, then application versions between, and including, the minimum and maximum versions specified in  <i>wszMinVersion</i> and <i>wszMaxVersion</i>, respectively, will be included or excluded.

### -param pfExclusion [out]

A pointer to a <b>BOOL</b> value that receives a value the specifies whether the policy is an exclusion policy. <b>TRUE</b> indicates that the application is prohibited from exercising the rights. <b>FALSE</b> indicates that the application is required to exercise the rights.

### -param puNameLength [in, out]

A pointer to a <b>UINT</b> value that, on entry, contains the length, in characters, of the <i>wszName</i> buffer. This length must include the terminating null character.

After the function returns, this value contains the number of characters, including the terminating null character, that were copied to the <i>wszName</i> buffer.

### -param wszName [out]

A pointer to a null-terminated Unicode string that receives the name of the application required to exercise or prohibited from exercising rights. The size of this buffer is specified by the <i>puNameLength</i> parameter.

To determine the required size of this buffer, pass <b>NULL</b> for this parameter. The function will place the size, in characters, including the terminating null character, in the <i>puNameLength</i> value.

### -param puMinVersionLength [in, out]

A pointer to a <b>UINT</b> value that, on entry, contains the length, in characters, of the <i>wszMinVersion</i> buffer. This length must include the terminating null character.

After the function returns, this value contains the number of characters, including the terminating null character, that were copied to the <i>wszMinVersion</i> buffer.

### -param wszMinVersion [out]

A pointer to a null-terminated Unicode string that receives the minimum version of the application required to exercise or prohibited from exercising rights. The size of this buffer is specified by the <i>puMinVersionLength</i> parameter.

To determine the required size of this buffer, pass <b>NULL</b> for this parameter. The function will place the size, in characters, including the terminating null character, in the <i>puMinVersionLength</i> value.

This will be a version string in a form similar to "1.0.1" or "1.00.0000".

### -param puMaxVersionLength [in, out]

A pointer to a <b>UINT</b> value that, on entry, contains the length, in characters, of the <i>wszMaxVersion</i> buffer. This length must include the terminating null character.

After the function returns, this value contains the number of characters, including the terminating null character, that were copied to the <i>wszMaxVersion</i> buffer.

### -param wszMaxVersion [out]

A pointer to a null-terminated Unicode string that receives the maximum version of the application required to exercise or prohibited from exercising rights. The size of this buffer is specified by the <i>puMaxVersionLength</i> parameter.

To determine the required size of this buffer, pass <b>NULL</b> for this parameter. The function will place the size, in characters, including the terminating null character, in the <i>puMaxVersionLength</i> value.

This will be a version string in a form similar to "1.0.1" or "1.00.0000".

### -param puPublicKeyLength [in, out]

A pointer to a <b>UINT</b> value that, on entry, contains the length, in characters, of the <i>wszPublicKey</i> buffer. This length must include the terminating null character.

After the function returns, this value contains the number of characters, including the terminating null character, that were copied to the <i>wszPublicKey</i> buffer.

### -param wszPublicKey [out]

A pointer to a null-terminated Unicode string that receives the public key used to sign the digest of the application required to exercise or prohibited from exercising rights. The key is a well-formed XrML node. The size of this buffer is specified by the <i>puPublicKeyLength</i> parameter.

To determine the required size of this buffer, pass <b>NULL</b> for this parameter. The function will place the size, in characters, including the terminating null character, in the <i>puPublicKeyLength</i> value.

### -param puDigestAlgorithmLength [in, out]

A pointer to a <b>UINT</b> value that, on entry, contains the length, in characters, of the <i>wszDigestAlgorithm</i> buffer. This length must include the terminating null character.

After the function returns, this value contains the number of characters, including the terminating null character, that were copied to the <i>wszDigestAlgorithm</i> buffer.

### -param wszDigestAlgorithm [out]

A pointer to a null-terminated Unicode string that receives the algorithm used to create the application digest that was specified in <i>pbDigest</i>. The size of this buffer is specified by the <i>puDigestAlgorithmLength</i> parameter.

To determine the required size of this buffer, pass <b>NULL</b> for this parameter. The function will place the size, in characters, including the terminating null character, in the <i>puDigestAlgorithmLength</i> value.

### -param pcbDigest [in, out]

A pointer to a <b>UINT</b> value that, on entry, contains the length, in bytes, of the <i>pbDigest</i> buffer.

After the function returns, this value contains the number of bytes copied to the <i>pbDigest</i> buffer.

### -param pbDigest [out]

A pointer to a buffer that receives the application digest that is required to exercise or prohibited from exercising rights. The size of this buffer is specified by the <i>pcbDigest</i> parameter.

To determine the required size of this buffer, pass <b>NULL</b> for this parameter. The function will place the size, in bytes, in the <i>pcbDigest</i> value.

## -returns

If the function succeeds, the function returns S_OK.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following list. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

Usage policies specify requirements or prohibitions for a client attempting to access content. For instance, a policy may specify that the file can only be opened with version 6.0 or higher of an application, or cannot be opened by another specific application. This function only returns data in parameters that apply to the usage policy type specified by <i>peUsagePolicyType</i>; values that are not applicable to the specified usage policy will not be returned, and buffers will not be required. However, an application can set an unlimited number of policies, so you can implement separate name, digest, and public key policies.

If version information is included, the consuming application must have version information or it will not be able to access the content.

Currently, comparison is a case-sensitive, character-by-character string comparison, so the values "6" and "6.0" are considered different. Because of this, an application must use a consistent format when setting and comparing values.

## -see-also

<a href="/previous-versions/windows/desktop/adrms_sdk/ad-rms-functions">AD RMS Functions</a>



<a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmsetusagepolicy">DRMSetUsagePolicy</a>