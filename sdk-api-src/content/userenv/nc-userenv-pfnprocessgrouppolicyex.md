---
UID: NC:userenv.PFNPROCESSGROUPPOLICYEX
title: PFNPROCESSGROUPPOLICYEX (userenv.h)
description: The ProcessGroupPolicyEx function is an application-defined callback function used when applying policy.
helpviewer_keywords: ["GPO_INFO_FLAG_ASYNC_FOREGROUND","GPO_INFO_FLAG_BACKGROUND","GPO_INFO_FLAG_FORCED_REFRESH","GPO_INFO_FLAG_LINKTRANSITION","GPO_INFO_FLAG_LOGRSOP_TRANSITION","GPO_INFO_FLAG_MACHINE","GPO_INFO_FLAG_NOCHANGES","GPO_INFO_FLAG_SAFEMODE_BOOT","GPO_INFO_FLAG_SLOWLINK","GPO_INFO_FLAG_VERBOSE","PFNPROCESSGROUPPOLICYEX","PFNPROCESSGROUPPOLICYEX callback","PFNPROCESSGROUPPOLICYEX callback function [Group Policy]","ProcessGroupPolicyEx","_win32_processgrouppolicyex","policy.processgrouppolicyex","userenv/PFNPROCESSGROUPPOLICYEX"]
old-location: policy\processgrouppolicyex.htm
tech.root: Policy
ms.assetid: df77fece-6e81-4a85-847a-fef3ba775e93
ms.date: 12/05/2018
ms.keywords: GPO_INFO_FLAG_ASYNC_FOREGROUND, GPO_INFO_FLAG_BACKGROUND, GPO_INFO_FLAG_FORCED_REFRESH, GPO_INFO_FLAG_LINKTRANSITION, GPO_INFO_FLAG_LOGRSOP_TRANSITION, GPO_INFO_FLAG_MACHINE, GPO_INFO_FLAG_NOCHANGES, GPO_INFO_FLAG_SAFEMODE_BOOT, GPO_INFO_FLAG_SLOWLINK, GPO_INFO_FLAG_VERBOSE, PFNPROCESSGROUPPOLICYEX, PFNPROCESSGROUPPOLICYEX callback, PFNPROCESSGROUPPOLICYEX callback function [Group Policy], ProcessGroupPolicyEx, _win32_processgrouppolicyex, policy.processgrouppolicyex, userenv/PFNPROCESSGROUPPOLICYEX
req.header: userenv.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PFNPROCESSGROUPPOLICYEX
 - userenv/PFNPROCESSGROUPPOLICYEX
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Userenv.h
api_name:
 - PFNPROCESSGROUPPOLICYEX
---

# PFNPROCESSGROUPPOLICYEX callback function


## -description

The <b>ProcessGroupPolicyEx</b> function is an 
  application-defined callback function used when applying policy. This extended function also supports the logging of 
  Resultant Set of Policy (RSoP) data. The <b>PFNPROCESSGROUPPOLICYEX</b> type defines a pointer 
  to this callback function. <b>ProcessGroupPolicyEx</b> 
  is a placeholder for the application-defined function name.

## -parameters

### -param dwFlags [in]

This parameter can be one or more of the following flags.



#### GPO_INFO_FLAG_MACHINE

Apply computer policy rather than user policy.



#### GPO_INFO_FLAG_BACKGROUND

Perform a background refresh of the policy. For more information, see the text following this list.



#### GPO_INFO_FLAG_ASYNC_FOREGROUND

Perform an asynchronous foreground refresh of policy. For more information, see the text following this 
        list. For more information about foreground policy application, see 
        <a href="/previous-versions/windows/desktop/Policy/initial-processing-of-group-policy">Initial Processing of Group Policy</a>.



#### GPO_INFO_FLAG_SLOWLINK

The policy is being applied across a slow link.



#### GPO_INFO_FLAG_VERBOSE

Write verbose output to the event log.



#### GPO_INFO_FLAG_NOCHANGES

No changes to the GPO were detected.



#### GPO_INFO_FLAG_LINKTRANSITION

A change in the link speed was detected between policy applications.



#### GPO_INFO_FLAG_LOGRSOP_TRANSITION

A change in RSoP logging was detected between the application of the previous policy and the application 
        of the current policy.



#### GPO_INFO_FLAG_FORCED_REFRESH

A forced policy refresh is being applied.



#### GPO_INFO_FLAG_SAFEMODE_BOOT

Safe mode flag.

The <b>GPO_INFO_FLAG_BACKGROUND</b> flag and the 
       <b>GPO_INFO_FLAG_ASYNC_FOREGROUND</b> flag can both be set. Because policies are always applied asynchronously during a 
<a href="/previous-versions/windows/desktop/Policy/background-refresh-of-group-policy">background refresh</a>, most extensions handle an asynchronous foreground refresh in the same manner in which they handle a background refresh. Therefore, they do not need to check for the <b>GPO_INFO_FLAG_ASYNC_FOREGROUND</b> flag. In instances when an extension must distinguish between a background refresh of policy and an asynchronous foreground refresh of policy, the extension can check for the <b>GPO_INFO_FLAG_ASYNC_FOREGROUND</b> flag.

### -param hToken [in]

Token for the user or computer, returned from the 
<a href="/windows/desktop/api/winbase/nf-winbase-logonusera">LogonUser</a>, 
<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createrestrictedtoken">CreateRestrictedToken</a>, 
<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-duplicatetoken">DuplicateToken</a>, 
<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocesstoken">OpenProcessToken</a>, or 
<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openthreadtoken">OpenThreadToken</a> function. This token must have <b>TOKEN_IMPERSONATE</b> and <b>TOKEN_QUERY</b> access. For more information, see 
<a href="/windows/desktop/SecAuthZ/access-rights-for-access-token-objects">Access Rights for Access-Token Objects</a> and 
<a href="/windows/desktop/SecAuthZ/client-impersonation">Client Impersonation</a>.

### -param hKeyRoot [in]

Handle to the <b>HKEY_LOCAL_MACHINE</b> or <b>HKEY_CURRENT_USER</b> registry key.

### -param pDeletedGPOList [in]

Pointer that receives the list of deleted GPO structures. For more information, see 
<a href="/windows/desktop/api/userenv/ns-userenv-group_policy_objecta">GROUP_POLICY_OBJECT</a>.

### -param pChangedGPOList [in]

Pointer that receives the list of changed GPO structures. For more information, see 
<a href="/windows/desktop/api/userenv/ns-userenv-group_policy_objecta">GROUP_POLICY_OBJECT</a>.

### -param pHandle [in]

Asynchronous completion handle. If the callback function does not support asynchronous processing, this handle is zero.

### -param *pbAbort [in]

Specifies whether to continue processing GPOs. If this parameter is <b>TRUE</b>, GPO processing will cease. If this parameter is <b>FALSE</b>, GPO processing will continue.

### -param pStatusCallback [in]

Pointer to a 
<a href="/windows/desktop/api/userenv/nc-userenv-pfnstatusmessagecallback">StatusMessageCallback</a> callback function that displays status messages. This parameter can be <b>NULL</b> in certain cases. For example, if the system is applying policy in the background, the status user interface is not present and the application cannot send status messages to be displayed. For more information, see the following Remarks section.

### -param *pWbemServices [in]

Specifies a WMI services pointer to the RSoP namespace to which the policy data should be written. This parameter is <b>NULL</b> when RSoP logging is disabled, indicating that the extension should not log RSoP data.

### -param *pRsopStatus [out]

Pointer to an <b>HRESULT</b> return code that indicates whether RSoP logging was successful.

## -returns

If policy was applied successfully, return <b>ERROR_SUCCESS</b>. If there are no changes to the GPO list, and the extension is to be called again, return <b>ERROR_OVERRIDE_NOCHANGES</b>. Returning <b>ERROR_OVERRIDE_NOCHANGES</b> ensures that the extension is called again, even if the <b>NoGPOListChanges</b> registry value is set. (For more information about this registry value, see Remarks.)

Return <b>ERROR_SYNC_FOREGROUND_REFRESH_REQUIRED</b> if the function was called for an asynchronous foreground refresh of policy but policy could not be applied during the asynchronous refresh. Returning <b>ERROR_SYNC_FOREGROUND_REFRESH_REQUIRED</b> indicates that the function must be called again for a synchronous foreground refresh of policy.

Otherwise, return a 
<a href="/windows/desktop/Debug/system-error-codes">system error code</a>.

## -remarks

For more information, see 
<a href="/previous-versions/windows/desktop/Policy/implementing-a-group-policy-client-side-extension">Implementing a Group Policy Client-side Extension</a>.

The system calls this function in the context of the 
<a href="/windows/desktop/Services/localsystem-account">LocalSystem account</a>, which has extensive privileges on the local computer. To use network resources, you must impersonate the user or computer by using the token provided in the <i>hToken</i> parameter.

To register this callback function, create a subkey under the following registry key:


<b>HKEY_LOCAL_MACHINE</b>&#92;<b>SOFTWARE</b>&#92;<b>Microsoft</b>&#92;<b>Windows NT</b>&#92;<b>CurrentVersion</b>&#92;<b>Winlogon</b>&#92;<b>GPExtensions</b>&#92;<b>ClientExtensionGuid</b>



The subkey should be a <b>GUID</b>, so that it is unique. It should contain the following values.



You should update the status message only if you are applying policy synchronously. This allows you to provide feedback and diagnostics during a lengthy policy application. To use the status message callback function, you must verify that <i>pStatusCallback</i> is not <b>NULL</b>. Then load your message string resource. When you call the status function, you must indicate whether the string is verbose. If the string is verbose, the callback function will verify that the computer is in verbose mode and display the message. For more information, see 
<a href="/windows/desktop/api/userenv/nc-userenv-pfnstatusmessagecallback">StatusMessageCallback</a>.

<div class="alert"><b>Warning</b>  Do not call the <i>pStatusCallback</i> function from a background thread or you may overwrite another thread's status message.</div>
<div> </div>

## -see-also

<a href="/previous-versions/windows/desktop/Policy/group-policy-functions">Group Policy
    Functions</a>



<a href="/previous-versions/windows/desktop/Policy/about-group-policy">Group Policy
    Overview</a>



<a href="/windows/desktop/api/userenv/nc-userenv-pfnprocessgrouppolicy">ProcessGroupPolicy</a>



<a href="/windows/desktop/api/userenv/nf-userenv-processgrouppolicycompletedex">ProcessGroupPolicyCompletedEx</a>



<a href="/previous-versions/windows/desktop/Policy/rsop-extensionstatus">RSOP_ExtensionStatus</a>



<a href="/windows/desktop/api/userenv/nf-userenv-refreshpolicy">RefreshPolicy</a>



<a href="/windows/desktop/api/userenv/nf-userenv-refreshpolicyex">RefreshPolicyEx</a>



<a href="/windows/desktop/api/userenv/nc-userenv-pfnstatusmessagecallback">StatusMessageCallback</a>