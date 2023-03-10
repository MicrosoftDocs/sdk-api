---
UID: NF:msdrm.DRMSetUsagePolicy
title: DRMSetUsagePolicy function (msdrm.h)
description: Sets a usage policy that requires or denies access to content based on application name, version, or other environment characteristics.
helpviewer_keywords: ["DRMSetUsagePolicy","DRMSetUsagePolicy function [Active Directory Rights Management Services SDK 1.0]","msdrm/DRMSetUsagePolicy","rm.drmsetusagepolicy"]
old-location: rm\drmsetusagepolicy.htm
tech.root: rm
ms.assetid: 8c270824-ff2a-4b04-b8b0-7cc4a82d042d
ms.date: 12/05/2018
ms.keywords: DRMSetUsagePolicy, DRMSetUsagePolicy function [Active Directory Rights Management Services SDK 1.0], msdrm/DRMSetUsagePolicy, rm.drmsetusagepolicy
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
 - DRMSetUsagePolicy
 - msdrm/DRMSetUsagePolicy
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
 - DRMSetUsagePolicy
---

# DRMSetUsagePolicy function


## -description

<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="/previous-versions/windows/desktop/msipc/microsoft-information-protection-and-control-client-portal">Active Directory Rights Management Services SDK 2.1</a>, 

which leverages functionality exposed by the client in Msipc.dll.]

The <b>DRMSetUsagePolicy</b> function sets a usage policy that requires or denies access to content based on application name, version, or other environment characteristics.

## -parameters

### -param hIssuanceLicense [in]

A handle to an issuance license.

### -param eUsagePolicyType [in]

One of the <a href="/windows/desktop/api/msdrmdefs/ne-msdrmdefs-drm_usagepolicy_type">DRM_USAGEPOLICY_TYPE</a> values that specifies the type of usage policy to be added or deleted. Only one type may be selected.

### -param fDelete [in]

Determines whether the policy should be added or removed. <b>TRUE</b> indicates the policy should be deleted. <b>FALSE</b> indicates the policy should be added.

### -param fExclusion [in]

Determines whether the application is prohibited from, or required to, exercise the rights. <b>FALSE</b> indicates that the application is required to exercise the rights. <b>TRUE</b> indicates that the application is prohibited from exercising the rights. You must specify <b>TRUE</b> if you set the <i>eUsagePolicyType</i> parameter to <b>DRM_USAGEPOLICY_TYPE_BYNAME</b> or <b>DRM_USAGEPOLICY_TYPE_BYDIGEST</b>.

### -param wszName [in]

A pointer to a null-terminated Unicode string that contains the name of the application. This parameter is required when <i>eUsagePolicyType</i> contains <b>DRM_USAGEPOLICY_TYPE_BYNAME</b>. It is ignored for all other <i>eUsagePolicyType</i> values.

### -param wszMinVersion [in]

A pointer to a null-terminated Unicode string that contains the minimum version of the application that is required to or prohibited from exercising rights. This should be a version string in a form similar to "1.0.1" or "1.00.0000". This parameter is required when <i>eUsagePolicyType</i> contains <b>DRM_USAGEPOLICY_TYPE_BYNAME</b> or <b>DRM_USAGEPOLICY_TYPE_OSEXCLUSION</b>. It is ignored for all other <i>eUsagePolicyType</i> values.

### -param wszMaxVersion [in]

A pointer to a null-terminated Unicode string that contains the maximum version of the application that is required to or prohibited from exercising rights. This should be a version string in a form similar to "1.0.1" or "1.00.0000". This parameter is required when <i>eUsagePolicyType</i> contains <b>DRM_USAGEPOLICY_TYPE_BYNAME</b> and optional when <i>eUsagePolicyType</i> contains <b>DRM_USAGEPOLICY_TYPE_OSEXCLUSION</b>. It is ignored for all other <i>eUsagePolicyType</i> values. If <i>eUsagePolicyType</i> contains <b>DRM_USAGEPOLICY_TYPE_OSEXCLUSION</b> and this parameter is specified, the version  must be greater than <i>wszMinVersion</i>.

### -param wszPublicKey [in]

A pointer to a null-terminated Unicode string that contains the public key used to sign the digest of the application required to or prohibited from exercising rights. This string must be a well-formed XrML node. This parameter is required when <i>eUsagePolicyType</i> contains <b>DRM_USAGEPOLICY_TYPE_BYPUBLICKEY</b>. It is ignored for all other <i>eUsagePolicyType</i> values.

### -param wszDigestAlgorithm [in]

A pointer to a null-terminated Unicode string that contains the algorithm used to create the application digest that is specified by <i>pbDigest</i>.  This parameter is required when <i>eUsagePolicyType</i> contains <b>DRM_USAGEPOLICY_TYPE_BYDIGEST</b>. It is ignored for all other <i>eUsagePolicyType</i> values.

### -param pbDigest [in]

A pointer to an array of bytes that contains the application digest required or prohibited from exercising rights. The size of this array is contained in the <i>cbDigest</i> parameter.  This parameter is required when <i>eUsagePolicyType</i> contains <b>DRM_USAGEPOLICY_TYPE_BYDIGEST</b>. It is ignored for all other <i>eUsagePolicyType</i> values.

### -param cbDigest [in]

The number of bytes in the <i>pbDigest</i> array.  This parameter is required when <i>eUsagePolicyType</i> contains <b>DRM_USAGEPOLICY_TYPE_BYDIGEST</b>. It is ignored for all other <i>eUsagePolicyType</i> values.

## -returns

If the function succeeds, the function returns S_OK.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following list. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

Usage policies allow or prevent a use license from being exercised by a specific application name or version, application public key, or application digest. For example, a policy may specify that the file can only be opened by version 6.0 or higher of an application, or that it may not be opened by a particular application. A usage policy can only be of one type (name, digest, or public key), which is specified by the <i>eUsagePolicyType</i> parameter; data entered that does not apply to the specified usage policy type is ignored. However, an application can set an unlimited number of policies, so you can implement separate name, digest, and public key policies.

When using this function, only the parameters required by the specific policy type need to have values; the other parameters should be <b>NULL</b>. The following list shows which parameters require values for which usage types. Note that all policy types require the <i>hIssuanceLicense</i>, <i>eUsagePolicyType</i>, <i>fDelete</i>, and <i>fExclusion</i> parameter values in addition to the following values.  
 <table>
<tr>
<th>eUsagePolicyType value</th>
<th>Required parameters</th>
</tr>
<tr>
<td><b>DRM_USAGEPOLICY_TYPE_BYNAME</b></td>
<td><i>wszName</i><i>wszMinVersion</i>

<i>wszMaxVersion</i>

</td>
</tr>
<tr>
<td><b>DRM_USAGEPOLICY_TYPE_BYPUBLICKEY</b></td>
<td><i>wszPublicKey</i></td>
</tr>
<tr>
<td><b>DRM_USAGEPOLICY_TYPE_BYDIGEST</b></td>
<td><i>wszDigestAlgorithm</i><i>pbDigest</i>

<i>cbDigest</i>

</td>
</tr>
<tr>
<td><b>DRM_USAGEPOLICY_TYPE_OSEXCLUSION</b></td>
<td><i>wszMinVersion</i> (Required.)<i>wszMaxVersion</i> (Optional. If used, must be greater than <i>wszMinVersion</i>.) These values are entered in the format <i>x.x.x.x</i>, where <i>x</i> represents an integer, typically from 1 to 4 digits long. So, for example, the version number for Windows XP with Service Pack 1 (SP1) would be "2.5.1.2600"; for Windows Server 2003, it would be "2.5.2.3790".

</td>
</tr>
</table>
 



The version comparison is a case-sensitive, character-by-character string comparison, so when comparing versions, "6" and "6.0" are considered different. Because of this, an application must use a consistent format when setting and comparing values.

## -see-also

<a href="/previous-versions/windows/desktop/adrms_sdk/ad-rms-functions">AD RMS Functions</a>



<a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmgetusagepolicy">DRMGetUsagePolicy</a>