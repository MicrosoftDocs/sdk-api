---
UID: NF:winsafer.SaferGetPolicyInformation
title: SaferGetPolicyInformation function (winsafer.h)
description: Gets information about a policy.
helpviewer_keywords: ["SAFER_SCOPEID_MACHINE","SAFER_SCOPEID_USER","SaferGetPolicyInformation","SaferGetPolicyInformation function [Security]","SaferPolicyDefaultLevel","SaferPolicyEnableTransparentEnforcement","SaferPolicyEvaluateUserScope","SaferPolicyLevelList","SaferPolicyScopeFlags","_mnp_safergetpolicyinformation","security.safergetpolicyinformation","winsafer/SaferGetPolicyInformation"]
old-location: security\safergetpolicyinformation.htm
tech.root: security
ms.assetid: 1c69d3c1-87e6-42cd-9acb-4c3d06801401
ms.date: 12/05/2018
ms.keywords: SAFER_SCOPEID_MACHINE, SAFER_SCOPEID_USER, SaferGetPolicyInformation, SaferGetPolicyInformation function [Security], SaferPolicyDefaultLevel, SaferPolicyEnableTransparentEnforcement, SaferPolicyEvaluateUserScope, SaferPolicyLevelList, SaferPolicyScopeFlags, _mnp_safergetpolicyinformation, security.safergetpolicyinformation, winsafer/SaferGetPolicyInformation
req.header: winsafer.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SaferGetPolicyInformation
 - winsafer/SaferGetPolicyInformation
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Advapi32.dll
api_name:
 - SaferGetPolicyInformation
req.apiset: ext-ms-win-advapi32-safer-l1-1-0 (introduced in Windows 8)
---

# SaferGetPolicyInformation function


## -description

The <b>SaferGetPolicyInformation</b> function gets information about a policy. You can query to find out more information about the policy.

## -parameters

### -param dwScopeId [in]

The scope of the query. The following table shows the possible values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SAFER_SCOPEID_MACHINE"></a><a id="safer_scopeid_machine"></a><dl>
<dt><b>SAFER_SCOPEID_MACHINE</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The scope of the query is by computer.

</td>
</tr>
<tr>
<td width="40%"><a id="SAFER_SCOPEID_USER"></a><a id="safer_scopeid_user"></a><dl>
<dt><b>SAFER_SCOPEID_USER</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
The scope of the query is by user.

</td>
</tr>
</table>

### -param SaferPolicyInfoClass [in]

A <a href="/windows/desktop/api/winsafer/ne-winsafer-safer_policy_info_class">SAFER_POLICY_INFO_CLASS</a>  enumeration value  that specifies the type of policy information that should be returned. The specified value determines the size and type of the <i>InfoBuffer</i> parameter. The following table shows the possible values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SaferPolicyLevelList"></a><a id="saferpolicylevellist"></a><a id="SAFERPOLICYLEVELLIST"></a><dl>
<dt><b>SaferPolicyLevelList</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Queries for the list of all levels defined in a policy.

<i>InfoBuffer</i> return type: <b>DWORD</b> array of LevelIds.

</td>
</tr>
<tr>
<td width="40%"><a id="SaferPolicyEnableTransparentEnforcement"></a><a id="saferpolicyenabletransparentenforcement"></a><a id="SAFERPOLICYENABLETRANSPARENTENFORCEMENT"></a><dl>
<dt><b>SaferPolicyEnableTransparentEnforcement</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Queries for the policy value to determine whether DLL checking is enabled.

<i>InfoBuffer</i> return type: <b>DWORD</b> Boolean.

</td>
</tr>
<tr>
<td width="40%"><a id="SaferPolicyDefaultLevel"></a><a id="saferpolicydefaultlevel"></a><a id="SAFERPOLICYDEFAULTLEVEL"></a><dl>
<dt><b>SaferPolicyDefaultLevel</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
Queries for the default policy level.

<i>InfoBuffer</i> return type: <b>DWORD</b> LevelId.

</td>
</tr>
<tr>
<td width="40%"><a id="SaferPolicyEvaluateUserScope"></a><a id="saferpolicyevaluateuserscope"></a><a id="SAFERPOLICYEVALUATEUSERSCOPE"></a><dl>
<dt><b>SaferPolicyEvaluateUserScope</b></dt>
<dt>4</dt>
</dl>
</td>
<td width="60%">
Queries to determine whether user scope rules should be consulted during policy evaluation.

<i>InfoBuffer</i> return type: <b>DWORD</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="SaferPolicyScopeFlags"></a><a id="saferpolicyscopeflags"></a><a id="SAFERPOLICYSCOPEFLAGS"></a><dl>
<dt><b>SaferPolicyScopeFlags</b></dt>
<dt>5</dt>
</dl>
</td>
<td width="60%">
Queries to determine whether the policy is to skip members of the local administrators group.

<i>InfoBuffer</i> return type: <b>DWORD</b>.

</td>
</tr>
</table>

### -param InfoBufferSize [in]

The size, in bytes, of the <i>InfoBuffer</i> parameter.

### -param InfoBuffer [out]

A buffer to contain the results of the query. The size and type of the returned information is determined by the <i>SaferPolicyInfoClass</i> parameter. For the type of the returned information for each possible value of the <i>SaferPolicyInfoClass</i> parameter, see the <i>SaferPolicyInfoClass</i> parameter.

### -param InfoBufferRetSize [out]

The number of bytes in the <i>InfoBuffer</i> parameter that were filled with policy information.

### -param lpReserved

Reserved for future use. This parameter should be set to <b>NULL</b>.

## -returns

<b>TRUE</b> if the function succeeds; otherwise, <b>FALSE</b>. For extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.
