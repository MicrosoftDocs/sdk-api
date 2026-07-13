---
UID: NF:lmaccess.NetValidatePasswordPolicy
title: NetValidatePasswordPolicy function (lmaccess.h)
description: The NetValidatePasswordPolicy function allows an application to check password compliance against an application-provided account database and verify that passwords meet the complexity, aging, minimum length, and history reuse requirements of a password policy.
helpviewer_keywords: ["NetValidateAuthentication","NetValidatePasswordChange","NetValidatePasswordPolicy","NetValidatePasswordPolicy function [Network Management]","NetValidatePasswordReset","lmaccess/NetValidatePasswordPolicy","netmgmt.netvalidatepasswordpolicy"]
old-location: netmgmt\netvalidatepasswordpolicy.htm
tech.root: NetMgmt
ms.assetid: be5ce51b-6568-49c8-954d-7b0d4bcb8611
ms.date: 12/05/2018
ms.keywords: NetValidateAuthentication, NetValidatePasswordChange, NetValidatePasswordPolicy, NetValidatePasswordPolicy function [Network Management], NetValidatePasswordReset, lmaccess/NetValidatePasswordPolicy, netmgmt.netvalidatepasswordpolicy
req.header: lmaccess.h
req.include-header: Lm.h
req.target-type: Windows
req.target-min-winverclnt: None supported
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
req.lib: Netapi32.lib
req.dll: Netapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - NetValidatePasswordPolicy
 - lmaccess/NetValidatePasswordPolicy
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Netapi32.dll
 - samcli.dll
api_name:
 - NetValidatePasswordPolicy
---

# NetValidatePasswordPolicy function


## -description

The <b>NetValidatePasswordPolicy</b> function allows an application to check password compliance against an application-provided account database and verify that passwords meet the complexity, aging, minimum length, and history reuse requirements of a password policy.

## -parameters

### -param ServerName [in]

A pointer to a constant Unicode string specifying the name of the remote server on which the function is to execute. This string must
        begin with \\ followed by the remote server name. If this parameter is <b>NULL</b>, the local computer is used.

### -param Qualifier [in]

Reserved for future use. This parameter must be <b>NULL</b>.

### -param ValidationType [in]

The type of password validation to perform. This parameter must be one of the following enumerated constant values. 





```cpp
typedef enum _NET_VALIDATE_PASSWORD_TYPE {

    NetValidateAuthentication = 1,
    NetValidatePasswordChange,
    NetValidatePasswordReset,

} NET_VALIDATE_PASSWORD_TYPE, *PNET_VALIDATE_PASSWORD_TYPE;

```


These values have the following meanings.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NetValidateAuthentication"></a><a id="netvalidateauthentication"></a><a id="NETVALIDATEAUTHENTICATION"></a><dl>
<dt><b>NetValidateAuthentication</b></dt>
</dl>
</td>
<td width="60%">
The application is requesting password validation during authentication. The <i>InputArg</i> parameter points to a <a href="/windows/win32/api/lmaccess/ns-lmaccess-net_validate_authentication_input_arg">NET_VALIDATE_AUTHENTICATION_INPUT_ARG</a> structure. This type of validation enforces password expiration and account lockout policy.

</td>
</tr>
<tr>
<td width="40%"><a id="NetValidatePasswordChange"></a><a id="netvalidatepasswordchange"></a><a id="NETVALIDATEPASSWORDCHANGE"></a><dl>
<dt><b>NetValidatePasswordChange</b></dt>
</dl>
</td>
<td width="60%">
The application is requesting password validation during a password change operation. The <i>InputArg</i> parameter points to a <a href="/windows/win32/api/lmaccess/ns-lmaccess-net_validate_password_change_input_arg">NET_VALIDATE_PASSWORD_CHANGE_INPUT_ARG</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="NetValidatePasswordReset"></a><a id="netvalidatepasswordreset"></a><a id="NETVALIDATEPASSWORDRESET"></a><dl>
<dt><b>NetValidatePasswordReset</b></dt>
</dl>
</td>
<td width="60%">
The application is requesting password validation during a password reset operation. The <i>InputArg</i> parameter points to a <a href="/windows/win32/api/lmaccess/ns-lmaccess-net_validate_password_reset_input_arg">NET_VALIDATE_PASSWORD_RESET_INPUT_ARG</a> structure. You can also reset the "lockout state" of a user account by specifying this structure.

</td>
</tr>
</table>

### -param InputArg [in]

A pointer to a structure that depends on the type of password validation to perform. The type of structure depends on the value of the <i>ValidationType</i> parameter. For more information, see the description of the <i>ValidationType</i> parameter.

### -param OutputArg [out]

If the <b>NetValidatePasswordPolicy</b> function succeeds (the return value is <b>Nerr_Success</b>), then the function
        allocates a buffer that contains the results of
        the operation. The <i>OutputArg</i> parameter contains a pointer to a <a href="/windows/desktop/api/lmaccess/ns-lmaccess-net_validate_output_arg">NET_VALIDATE_OUTPUT_ARG</a> structure. The application must examine <b>ValidationStatus</b> member in the <b>NET_VALIDATE_OUTPUT_ARG</b> structure pointed to by the <i>OutputArg</i> parameter to
        determine the results of the password policy validation check.   The <b>NET_VALIDATE_OUTPUT_ARG</b> structure contains a <a href="/windows/desktop/api/lmaccess/ns-lmaccess-net_validate_persisted_fields">NET_VALIDATE_PERSISTED_FIELDS</a> structure with changes to persistent password-related information, and the results of the password validation. The application must
        plan to persist all persisted the fields in the <b>NET_VALIDATE_PERSISTED_FIELDS</b> structure aside from the <b>ValidationStatus</b> member as information along with the user object information and provide the required fields from
        the persisted information when calling this function in the future on the same user object.

If the <b>NetValidatePasswordPolicy</b> function fails (the return value is nonzero),  then <i>OutputArg</i> parameter is set to a <b>NULL</b> pointer and password policy
        could not be examined.

For more information, see the Return Values and Remarks sections.

## -returns

If the function succeeds, and the password is authenticated, changed, or reset, the return value is NERR_Success and the function allocates an <i>OutputArg</i> parameter.

If the function fails, the <i>OutputArg</i> parameter is <b>NULL</b> and the return value is a system error code that can be one of the following error codes. For a list of all possible error codes, see 
<a href="/windows/desktop/Debug/system-error-codes">System Error Codes</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
A parameter is incorrect. This error is returned if the <i>InputArg</i>  or <i>OutputArg</i> parameters are <b>NULL</b>. This error is also returned if the <i>Qualifier</i> parameter is not <b>NULL</b> or if the <i>ValidationType</i> parameter is not one of the allowed values. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
Not enough memory is available to complete the operation.

</td>
</tr>
</table>

## -remarks

The <b>NetValidatePasswordPolicy</b> function is designed to allow applications to validate passwords for users that are in an account database provided by the application. This function can also be used to verify that passwords meet the complexity, aging, minimum length, and history reuse requirements of a password policy. This function also provides the means for an application to implement an account-lockout mechanism.

The <b>NetValidatePasswordPolicy</b> function does not validate passwords in Active Directory accounts and cannot be used for this purpose.
The only policy that this function checks a password against in Active Directory accounts is the password complexity (the password strength). 

A typical scenario for the use of the <b>NetValidatePasswordPolicy</b> function would be enforcing the choice of strong passwords by users for web applications and applications that allow password-protected documents. Another use of this function could be checking password complexity in a situation in which a password is attached to a functional operation rather than to a user account; for example, passwords that are used with Secure Multipurpose Internet Mail Extensions (S/MIME) certificate-based public keys.

If the <b>NetValidatePasswordPolicy</b> function is called on a domain controller that is running Active Directory, access is allowed or denied based on the ACL for the <a href="/windows/desktop/SecAuthZ/securable-objects">securable object</a>. The default ACL permits all authenticated users and members of the "<a href="/windows/desktop/SecAuthZ/allowing-anonymous-access">Pre-Windows 2000 compatible access</a>" group to view the information. If you call this function on a member server or workstation, all authenticated users can view the information. For  information about anonymous access and restricting anonymous access on these platforms, see 
<a href="/windows/desktop/NetMgmt/security-requirements-for-the-network-management-functions">Security Requirements for the Network Management Functions</a>. For more information on ACLs, ACEs, and access tokens, see 
<a href="/windows/desktop/SecAuthZ/access-control-model">Access Control Model</a>.

The security descriptor of the Domain object is used to perform the access check for the <b>NetValidatePasswordPolicy</b> function. 

To call <b>NetValidatePasswordPolicy</b> in a security context that is not the default, first call the <a href="/windows/desktop/api/winbase/nf-winbase-logonusera">LogonUser</a> function, specifying LOGON32_LOGON_NEW_CREDENTIALS in the <i>dwLogonType</i> parameter, and then call <b>NetValidatePasswordPolicy</b> under impersonation. For more information about impersonation, see <a href="/windows/desktop/SecAuthZ/client-impersonation">Client Impersonation</a>.

If the return code of the <b>NetValidatePasswordPolicy</b> function is <b>Nerr_Success</b> then the function
        allocates a buffer pointed to by the <i>OutputArg</i> parameter that contains a <a href="/windows/desktop/api/lmaccess/ns-lmaccess-net_validate_output_arg">NET_VALIDATE_OUTPUT_ARG</a> structure with the results of
        the operation. The application must examine <b>ValidationStatus</b> member in the <b>NET_VALIDATE_OUTPUT_ARG</b> structure to
        determine the results of the password policy validation check.  For more information, see <b>NET_VALIDATE_OUTPUT_ARG</b>.

Note that it is the application's responsibility to save all the data in the <b>ChangedPersistedFields</b> member of the <b>NET_VALIDATE_OUTPUT_ARG</b> structure as well as any User object information. The next time the application calls <b>NetValidatePasswordPolicy</b> on the same instance of the User object, the application must provide the required fields from the persistent information.

When you call <b>NetValidatePasswordPolicy</b> and specify <a href="/windows/win32/api/lmaccess/ns-lmaccess-net_validate_password_change_input_arg">NET_VALIDATE_PASSWORD_CHANGE_INPUT_ARG</a> or <a href="/windows/desktop/api/lmaccess/ns-lmaccess-net_validate_password_reset_input_arg">NET_VALIDATE_PASSWORD_RESET_INPUT_ARG</a> in <i>InputArg</i> parameter, the call also validates the password by passing it through the password filter DLL that the computer is configured to use. For more information about password filters, see <a href="/windows/desktop/SecMgmt/using-password-filters">Using Password Filters</a>.

If the return value from the <b>NetValidatePasswordPolicy</b> function is nonzero then <i>OutputArg</i> parameter  is set to <b>NULL</b> and password policy
        could not be examined.

The <a href="/windows/desktop/api/lmaccess/nf-lmaccess-netvalidatepasswordpolicyfree">NetValidatePasswordPolicyFree</a> function should be called after calling  <b>NetValidatePasswordPolicy</b> to free the memory allocated for the <i>OutputArg</i> parameter that is returned by the call to the <b>NetValidatePasswordPolicy</b> function.

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-logonusera">LogonUser</a>



<a href="/windows/win32/api/lmaccess/ns-lmaccess-net_validate_authentication_input_arg">NET_VALIDATE_AUTHENTICATION_INPUT_ARG</a>



<b>NET_VALIDATE_OUTPUT_ARG</b>



<a href="/windows/win32/api/lmaccess/ns-lmaccess-net_validate_password_change_input_arg">NET_VALIDATE_PASSWORD_CHANGE_INPUT_ARG</a>



<a href="/windows/win32/api/lmaccess/ns-lmaccess-net_validate_password_reset_input_arg">NET_VALIDATE_PASSWORD_RESET_INPUT_ARG</a>



<a href="/windows/desktop/api/lmaccess/ns-lmaccess-net_validate_persisted_fields">NET_VALIDATE_PERSISTED_FIELDS</a>



<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netvalidatepasswordpolicyfree">NetValidatePasswordPolicyFree</a>



<a href="/windows/desktop/NetMgmt/network-management-functions">Network
		  Management Functions</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management
		  Overview</a>