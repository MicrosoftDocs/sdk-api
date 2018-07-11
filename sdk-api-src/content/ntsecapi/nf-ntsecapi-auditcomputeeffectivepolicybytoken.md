---
UID: NF:ntsecapi.AuditComputeEffectivePolicyByToken
title: AuditComputeEffectivePolicyByToken function
author: windows-sdk-content
description: Computes the effective audit policy for one or more subcategories for the security principal associated with the specified token. The function computes effective audit policy by combining system audit policy with per-user policy.
old-location: security\auditcomputeeffectivepolicybytoken_func.htm
old-project: secauthz
ms.assetid: e5fc9b8d-a61e-48c2-9093-f27167232cc8
ms.author: windowssdkdev
ms.date: 07/04/2018
ms.keywords: AuditComputeEffectivePolicyByToken, AuditComputeEffectivePolicyByToken function [Security], ntsecapi/AuditComputeEffectivePolicyByToken, security.auditcomputeeffectivepolicybytoken_func
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: ntsecapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: TRUSTED_INFORMATION_CLASS, *PTRUSTED_INFORMATION_CLASS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Advapi32.dll
api_name:
 - AuditComputeEffectivePolicyByToken
product: Windows
targetos: Windows
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
req.product: ADAM
---

# AuditComputeEffectivePolicyByToken function


## -description


The <b>AuditComputeEffectivePolicyByToken</b> function computes the effective audit policy for one or more subcategories for the security principal associated with the specified token. The function computes effective audit policy by combining system audit policy with per-user policy. 


## -parameters




### -param hTokenHandle [in]

A handle to the access token associated with the principal for which to compute effective audit policy. The token must have been opened with <b>TOKEN_QUERY</b> access. Per-user policy for group SIDs is not currently supported.


### -param pSubCategoryGuids [in]

A pointer to an array of <b>GUID</b> values that specify the subcategories for which to compute effective audit policy. For a list of defined subcategories, see <a href="https://msdn.microsoft.com/e3b12139-947d-4922-91fd-f9833c069011">Auditing Constants</a>.


### -param dwPolicyCount

TBD


### -param ppAuditPolicy [out]

A pointer to a single buffer that contains both an array of pointers to <a href="https://msdn.microsoft.com/3fafeec9-a028-4a65-933e-fb973eb257b0">AUDIT_POLICY_INFORMATION</a> structures and the structures themselves. The <b>AUDIT_POLICY_INFORMATION</b> structures specify the effective audit policy for the subcategories specified by the <i>pSubCategoryGuids</i> array. 

When you have finished using this buffer, free it by calling the <a href="https://msdn.microsoft.com/697baf9b-91c4-4a88-a190-e9f6812e08af">AuditFree</a> function.


#### - PolicyCount [in]

The number of elements in each of the <i>pSubCategoryGuids</i> and <i>ppAuditPolicy</i> arrays.


## -returns




						If the function succeeds, it returns <b>TRUE</b>.

If the function fails, it returns <b>FALSE</b>. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. <b>GetLastError</b> may return one of the following error codes defined in WinError.h.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DENIED</b></dt>
<dt>5</dt>
</dl>
</td>
<td width="60%">
The caller does not have the privilege or access rights necessary to call this function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
<dt>87</dt>
</dl>
</td>
<td width="60%">
One or more parameters are invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_FILE_NOT_FOUND</b></dt>
<dt>2 (0x2)</dt>
</dl>
</td>
<td width="60%">
No per-user audit policy exists for the principal specified by the <i>pSid</i> parameter.

</td>
</tr>
</table>
 




## -remarks



To successfully call this function, the caller must have <b>SeSecurityPrivilege</b> or have both <b>AUDIT_QUERY_SYSTEM_POLICY</b> and <b>AUDIT_QUERY_USER_POLICY</b> access on the <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">Audit security object</a>.



