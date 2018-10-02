---
UID: NF:ntsecapi.AuditComputeEffectivePolicyBySid
title: AuditComputeEffectivePolicyBySid function
author: windows-sdk-content
description: Computes the effective audit policy for one or more subcategories for the specified security principal. The function computes effective audit policy by combining system audit policy with per-user policy.
old-location: security\auditcomputeeffectivepolicybysid_func.htm
tech.root: SecAuthZ
ms.assetid: cac928e5-8d8f-4b2f-9c1b-c00dc891e3d1
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: AuditComputeEffectivePolicyBySid, AuditComputeEffectivePolicyBySid function [Security], ntsecapi/AuditComputeEffectivePolicyBySid, security.auditcomputeeffectivepolicybysid_func
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Advapi32.dll
 - API-MS-Win-Security-audit-l1-1-0.dll
 - sechost.dll
 - API-MS-Win-Security-audit-l1-1-1.dll
api_name:
 - AuditComputeEffectivePolicyBySid
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# AuditComputeEffectivePolicyBySid function


## -description


The <b>AuditComputeEffectivePolicyBySid</b> function computes the effective audit policy for one or more subcategories for the specified security principal. The function computes effective audit policy by combining system audit policy with per-user policy. 


## -parameters




### -param pSid [in]

A pointer to the <a href="https://msdn.microsoft.com/328fba4e-e590-4174-9274-52dad58cb91f">SID</a> structure associated with the principal for which to compute effective audit policy. Per-user policy for group SIDs is not currently supported.


### -param pSubCategoryGuids [in]

A pointer to an array of <b>GUID</b> values that specify the subcategories for which to compute effective audit policy. For a list of defined subcategories, see <a href="https://msdn.microsoft.com/e3b12139-947d-4922-91fd-f9833c069011">Auditing Constants</a>.


### -param dwPolicyCount [in]

The number of elements in each of the <i>pSubCategoryGuids</i> and <i>ppAuditPolicy</i> arrays.


### -param ppAuditPolicy [out]

A pointer to a single buffer that contains both an array of pointers to <a href="https://msdn.microsoft.com/3fafeec9-a028-4a65-933e-fb973eb257b0">AUDIT_POLICY_INFORMATION</a> structures and the structures themselves. The <b>AUDIT_POLICY_INFORMATION</b> structures specify the effective audit policy for the subcategories specified by the <i>pSubCategoryGuids</i> array. 

When you have finished using this buffer, free it by calling the <a href="https://msdn.microsoft.com/697baf9b-91c4-4a88-a190-e9f6812e08af">AuditFree</a> function.


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
<dt>87 (0x57)</dt>
</dl>
</td>
<td width="60%">
One or more parameters are not valid.

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



To successfully call this function, the caller must have <b>SeSecurityPrivilege</b> or have <b>AUDIT_QUERY_SYSTEM_POLICY</b> and <b>AUDIT_QUERY_USER_POLICY</b> access on the <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">Audit security object</a>.



