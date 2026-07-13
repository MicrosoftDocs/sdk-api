---
UID: NF:wincred.CredUICmdLinePromptForCredentialsA
title: CredUICmdLinePromptForCredentialsA function (wincred.h)
description: Prompts for and accepts credential information from a user working in a command-line (console) application. The name and password typed by the user are passed back to the calling application for verification. (ANSI)
helpviewer_keywords: ["CREDUI_FLAGS_ALWAYS_SHOW_UI", "CREDUI_FLAGS_DO_NOT_PERSIST", "CREDUI_FLAGS_EXCLUDE_CERTIFICATES", "CREDUI_FLAGS_EXPECT_CONFIRMATION", "CREDUI_FLAGS_GENERIC_CREDENTIALS", "CREDUI_FLAGS_INCORRECT_PASSWORD", "CREDUI_FLAGS_PERSIST", "CREDUI_FLAGS_REQUEST_ADMINISTRATOR", "CREDUI_FLAGS_REQUIRE_CERTIFICATE", "CREDUI_FLAGS_REQUIRE_SMARTCARD", "CREDUI_FLAGS_SERVER_CREDENTIAL", "CREDUI_FLAGS_SHOW_SAVE_CHECK_BOX", "CREDUI_FLAGS_USERNAME_TARGET_CREDENTIALS", "CredUICmdLinePromptForCredentialsA", "wincred/CredUICmdLinePromptForCredentialsA"]
old-location: security\creduicmdlinepromptforcredentials.htm
tech.root: security
ms.assetid: 5b5bfe87-8f31-4228-931e-50cfc399b66b
ms.date: 12/05/2018
ms.keywords: CREDUI_FLAGS_ALWAYS_SHOW_UI, CREDUI_FLAGS_DO_NOT_PERSIST, CREDUI_FLAGS_EXCLUDE_CERTIFICATES, CREDUI_FLAGS_EXPECT_CONFIRMATION, CREDUI_FLAGS_GENERIC_CREDENTIALS, CREDUI_FLAGS_INCORRECT_PASSWORD, CREDUI_FLAGS_PERSIST, CREDUI_FLAGS_REQUEST_ADMINISTRATOR, CREDUI_FLAGS_REQUIRE_CERTIFICATE, CREDUI_FLAGS_REQUIRE_SMARTCARD, CREDUI_FLAGS_SERVER_CREDENTIAL, CREDUI_FLAGS_SHOW_SAVE_CHECK_BOX, CREDUI_FLAGS_USERNAME_TARGET_CREDENTIALS, CredUICmdLinePromptForCredentials, CredUICmdLinePromptForCredentials function [Security], CredUICmdLinePromptForCredentialsA, CredUICmdLinePromptForCredentialsW, _cred_creduicmdlinepromptforcredentials, security.creduicmdlinepromptforcredentials, wincred/CredUICmdLinePromptForCredentials, wincred/CredUICmdLinePromptForCredentialsA, wincred/CredUICmdLinePromptForCredentialsW
req.header: wincred.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CredUICmdLinePromptForCredentialsW (Unicode) and CredUICmdLinePromptForCredentialsA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Credui.lib
req.dll: Credui.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CredUICmdLinePromptForCredentialsA
 - wincred/CredUICmdLinePromptForCredentialsA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Credui.dll
 - Ext-MS-Win-security-credui-l1-1-0.dll
 - Ext-MS-Win-security-credui-l1-1-1.dll
 - AnalogCredUI.dll
api_name:
 - CredUICmdLinePromptForCredentials
 - CredUICmdLinePromptForCredentialsA
 - CredUICmdLinePromptForCredentialsW
---

# CredUICmdLinePromptForCredentialsA function


## -description

The <b>CredUICmdLinePromptForCredentials</b> function prompts for and accepts credential information from a user working in a command-line (console) application. The name and password typed by the user are passed back to the calling application for verification.

## -parameters

### -param pszTargetName [in]

A pointer to a <b>null</b>-terminated string that contains the name of the target for the credentials, typically a server name. For DFS connections, this string is of the form <i>ServerName</i><b>\\</b><i>ShareName</i>. The <i>pszTargetName</i> parameter is used to identify the target information and is used to store and retrieve the credential.

### -param pContext [in]

Currently reserved and must be <b>NULL</b>.

### -param dwAuthError [in, optional]

Specifies why prompting for credentials is needed. A caller can pass this Windows error parameter, returned by another authentication call, to allow the dialog box to accommodate certain errors. For example, if the password expired status code is passed, the dialog box prompts the user to change the password on the account.

### -param UserName [in, out]

A pointer to a <b>null</b>-terminated string that contains the credential user name. If a nonzero-length string is specified for <i>pszUserName</i>, the user will be prompted only for the password. In the case of credentials other than user name/password, a marshaled format of the credential can be passed in. This string is created by calling 
<a href="/windows/desktop/api/wincred/nf-wincred-credmarshalcredentiala">CredMarshalCredential</a>. 




This function writes the user-supplied name to this buffer, copying a maximum of <i>ulUserNameMaxChars</i> characters. The string in this format can be converted to the user name/password format by calling the 
<a href="/windows/desktop/api/wincred/nf-wincred-creduiparseusernamea">CredUIParseUsername</a> function. The string in its marshaled format can be passed directly to a <a href="/windows/desktop/SecGloss/s-gly">security support provider</a> (SSP).

If the CREDUI_FLAGS_DO_NOT_PERSIST flag is not specified, the value returned in this parameter is of a form that should not be inspected, printed, or persisted other than passing it to <a href="/windows/desktop/api/wincred/nf-wincred-creduiparseusernamea">CredUIParseUsername</a>. The subsequent results of <b>CredUIParseUsername</b> can  be passed only to a client-side authentication API such as <a href="/windows/desktop/api/winnetwk/nf-winnetwk-wnetaddconnectiona">WNetAddConnection</a> or the SSP API.

### -param ulUserBufferSize [in]

The maximum number of characters that can be copied to <i>pszUserName</i> including the terminating <b>null</b> character. 




<div class="alert"><b>Note</b>  CREDUI_MAX_USERNAME_LENGTH does not include the terminating <b>null</b> character.</div>
<div> </div>

### -param pszPassword [in, out]

A pointer to a <b>null</b>-terminated string that contains the password for the credentials. If a nonzero-length string is specified for <i>pszPassword</i>, the password parameter will be prefilled with the string. 




This function writes the user-supplied password to this buffer, copying a maximum of <i>ulPasswordMaxChars</i> characters. If the CREDUI_FLAGS_DO_NOT_PERSIST flag is not specified, the value returned in this parameter is of a form that should not be inspected, printed, or persisted other than passing it to a client-side authentication function such as <a href="/windows/desktop/api/winnetwk/nf-winnetwk-wnetaddconnectiona">WNetAddConnection</a> or an SSP function.

When you have finished using the password, clear the password from memory by calling the <a href="/previous-versions/windows/desktop/legacy/aa366877(v=vs.85)">SecureZeroMemory</a> function. For more information about protecting passwords, see <a href="/windows/desktop/SecBP/handling-passwords">Handling Passwords</a>.

### -param ulPasswordBufferSize [in]

The maximum number of characters that can be copied to <i>pszPassword</i> including the terminating <b>null</b> character. 




<div class="alert"><b>Note</b>  CREDUI_MAX_PASSWORD_LENGTH does not include the terminating <b>null</b> character.</div>
<div> </div>

### -param pfSave [in, out]

A pointer to a <b>BOOL</b> that specifies the initial state of the <b>Save</b> message and receives the state of the <b>Save</b> message after the user has responded to the command prompt. If <i>pfSave</i> is not <b>NULL</b> and <a href="/windows/desktop/api/wincred/nf-wincred-creduipromptforcredentialsa">CredUIPromptForCredentials</a> returns NO_ERROR, <i>pfSave</i> returns the state of the <b>Save</b> message. If the CREDUI_FLAGS_PERSIST flag is specified, the <b>Save</b> message is not displayed but is considered to be "y". If the CREDUI_FLAGS_DO_NOT_PERSIST flag is specified and CREDUI_FLAGS_SHOW_SAVE_CHECK_BOX is not specified, the <b>Save</b> message is not displayed but is considered to be "n".

### -param dwFlags [in]

A <b>DWORD</b> value that specifies special behavior for this function. This value can be a bitwise-<b>OR</b> combination of zero or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CREDUI_FLAGS_ALWAYS_SHOW_UI"></a><a id="credui_flags_always_show_ui"></a><dl>
<dt><b>CREDUI_FLAGS_ALWAYS_SHOW_UI</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Display a user interface if the credentials can be returned from an existing credential in credential manager. This flag is  permitted only if CREDUI_FLAGS_GENERIC_CREDENTIALS is also specified and is  used only in conjunction with CREDUI_FLAGS_GENERIC_CREDENTIALS.

</td>
</tr>
<tr>
<td width="40%"><a id="CREDUI_FLAGS_DO_NOT_PERSIST"></a><a id="credui_flags_do_not_persist"></a><dl>
<dt><b>CREDUI_FLAGS_DO_NOT_PERSIST</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Do not display the save message or store credentials.

CREDUI_FLAGS_SHOW_SAVE_CHECK_BOX can also be passed to display the save message only and return the result in <i>pfSave</i>.

</td>
</tr>
<tr>
<td width="40%"><a id="CREDUI_FLAGS_EXCLUDE_CERTIFICATES"></a><a id="credui_flags_exclude_certificates"></a><dl>
<dt><b>CREDUI_FLAGS_EXCLUDE_CERTIFICATES</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Prompt for user name/password. If the <i>pszUserName</i> parameter is specified, the user name is omitted. If the credential is persisted, store the passed-in user name with the credential.

</td>
</tr>
<tr>
<td width="40%"><a id="CREDUI_FLAGS_EXPECT_CONFIRMATION"></a><a id="credui_flags_expect_confirmation"></a><dl>
<dt><b>CREDUI_FLAGS_EXPECT_CONFIRMATION</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Specifies that the caller will call 
<a href="/windows/desktop/api/wincred/nf-wincred-creduiconfirmcredentialsa">CredUIConfirmCredentials</a> to determine whether the returned credentials are actually valid. This ensures that credentials that are not valid are not saved to the credential manager. Specify this flag unless CREDUI_FLAGS_DO_NOT_PERSIST is specified.

</td>
</tr>
<tr>
<td width="40%"><a id="CREDUI_FLAGS_GENERIC_CREDENTIALS"></a><a id="credui_flags_generic_credentials"></a><dl>
<dt><b>CREDUI_FLAGS_GENERIC_CREDENTIALS</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Consider the credentials entered by the user a generic credential.

</td>
</tr>
<tr>
<td width="40%"><a id="CREDUI_FLAGS_INCORRECT_PASSWORD"></a><a id="credui_flags_incorrect_password"></a><dl>
<dt><b>CREDUI_FLAGS_INCORRECT_PASSWORD</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Silently ignore this flag.

</td>
</tr>
<tr>
<td width="40%"><a id="CREDUI_FLAGS_PERSIST"></a><a id="credui_flags_persist"></a><dl>
<dt><b>CREDUI_FLAGS_PERSIST</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Do not show the save message, but save the credential as though the user answered "y".

</td>
</tr>
<tr>
<td width="40%"><a id="CREDUI_FLAGS_REQUEST_ADMINISTRATOR"></a><a id="credui_flags_request_administrator"></a><dl>
<dt><b>CREDUI_FLAGS_REQUEST_ADMINISTRATOR</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Silently ignore this flag.

</td>
</tr>
<tr>
<td width="40%"><a id="CREDUI_FLAGS_REQUIRE_CERTIFICATE"></a><a id="credui_flags_require_certificate"></a><dl>
<dt><b>CREDUI_FLAGS_REQUIRE_CERTIFICATE</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Reserved for future use; do not pass this flag.

</td>
</tr>
<tr>
<td width="40%"><a id="CREDUI_FLAGS_REQUIRE_SMARTCARD"></a><a id="credui_flags_require_smartcard"></a><dl>
<dt><b>CREDUI_FLAGS_REQUIRE_SMARTCARD</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Use a smart card and prompt for a PIN. If more than one smart card is available, select one of them. If the <i>pszUserName</i> parameter passes a string that is not empty, the string must match the UPN associated with the certificate on one of the smart cards. A UPN matches if the string matches the whole UPN on the certificate or the string matches the part to the left of the at sign (@) in the UPN of the certificate. If there is a match, the matching smart card is selected.

</td>
</tr>
<tr>
<td width="40%"><a id="CREDUI_FLAGS_SERVER_CREDENTIAL"></a><a id="credui_flags_server_credential"></a><dl>
<dt><b>CREDUI_FLAGS_SERVER_CREDENTIAL</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
This flag is meaningful only in locating a matching credential to prefill the dialog box, should authentication fail.  When this flag is specified, wildcard credentials will not be matched. It has no effect when writing a credential. CredUI does not create credentials that contain wildcard characters.  Any found were either created explicitly by the user
or created programmatically, as happens when a RAS connection is made.

</td>
</tr>
<tr>
<td width="40%"><a id="CREDUI_FLAGS_SHOW_SAVE_CHECK_BOX"></a><a id="credui_flags_show_save_check_box"></a><dl>
<dt><b>CREDUI_FLAGS_SHOW_SAVE_CHECK_BOX</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Display the save message and return <b>TRUE</b> in the <i>pfSave</i> out parameter if the user answers "y", <b>FALSE</b> if the user answers "n". CREDUI_FLAGS_DO_NOT_PERSIST must be specified to use this flag.

</td>
</tr>
<tr>
<td width="40%"><a id="CREDUI_FLAGS_USERNAME_TARGET_CREDENTIALS"></a><a id="credui_flags_username_target_credentials"></a><dl>
<dt><b>CREDUI_FLAGS_USERNAME_TARGET_CREDENTIALS</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The credential is a run-as credential. The <i>pszTargetName</i> parameter specifies the name of the command or program being run. It is used for prompting purposes only.

</td>
</tr>
</table>

## -returns

The return value is a <b>DWORD</b> and can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_FLAGS</b></dt>
</dl>
</td>
<td width="60%">
This status is returned for any of the flag combinations that are not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
Either <i>pszTargetName</i> is <b>NULL</b>, the empty string, or longer than CREDUI_MAX_DOMAIN_LENGTH, or <i>pUiInfo</i> is not <b>NULL</b> and the <a href="/windows/desktop/api/wincred/ns-wincred-credui_infoa">CredUI_INFO</a> structure pointed to did not meet one of the following requirements: 

<ul>
<li>The <b>cbSize</b> member must be one.</li>
<li>If the <b>hbmBanner</b> member is not <b>NULL</b>, it must be of type OBJ_BITMAP.</li>
<li>If the <b>pszMessageText</b> member is not <b>NULL</b>, it must not be greater than CREDUI_MAX_MESSAGE_LENGTH.</li>
<li>If the <b>pszCaptionText</b> member is not <b>NULL</b>, it must not be greater than CREDUI_MAX_CAPTION_LENGTH.</li>
</ul>
</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_SUCH_LOGON_SESSION</b></dt>
</dl>
</td>
<td width="60%">
The credential manager cannot be used. Typically, this error is handled by calling <a href="/windows/desktop/api/wincred/nf-wincred-creduicmdlinepromptforcredentialsa">CredUICmdLinePromptForCredentials</a> and passing in the CREDUI_FLAGS_DO_NOT_PERSIST flag.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NO_ERROR</b></dt>
</dl>
</td>
<td width="60%">
User chose <b>OK</b>. The <i>pszUserName</i>, <i>pszPassword</i>, and <i>pfSave</i> variables will return the values documented earlier.

</td>
</tr>
</table>

## -remarks

The CREDUI_FLAGS_REQUIRE_SMARTCARD, CREDUI_FLAGS_REQUIRE_CERTIFICATE, and CREDUI_FLAGS_EXCLUDE_CERTIFICATE flags are mutually exclusive.

If CREDUI_FLAGS_DO_NOT_PERSIST is specified, either <i>pszTargetName</i> must be specified or  <i>uiInfo-&gt;pszMessageText</i> and <i>uiInfo-&gt;pszCaption</i> must be specified.

The CREDUI_FLAG_USERNAME_TARGET_CREDENTIALS and CREDUI_FLAGS_GENERIC_CREDENTIALS flags are mutually exclusive. If neither is specified, the credential is a domain credential.

If CREDUI_FLAGS_GENERIC_CREDENTIALS is not specified or CREDUI_FLAGS_COMPLETE_USERNAME is specified, the typed name is <i>syntax checked</i>. Syntax checked means that the same rules are used as are implied by <a href="/windows/desktop/api/wincred/nf-wincred-creduiparseusernamea">CredUIParseUserName</a>. If the typed name is not valid, the user is prompted for a valid one. If the domain portion of the typed name is missing, one will be supplied based on the target name.

If CREDUI_FLAGS_GENERIC_CREDENTIALS is specified and CREDUI_FLAGS_VALIDATE_USERNAME is also specified, the typed name is syntax checked. If the typed name is not valid, the user is prompted for a valid one.

If CREDUI_FLAGS_GENERIC_CREDENTIALS is specified and neither CREDUI_FLAGS_COMPLETE_USERNAME nor CREDUI_FLAGS_VALIDATE_USERNAME is specified, the typed name is not syntax checked in any way.

If neither CREDUI_FLAGS_PERSIST nor CREDUI_FLAGS_DO_NOT_PERSIST are set, the save message is shown, and it controls whether the credential is saved or not.

If CREDUI_FLAGS_PROMPT_FOR_SAVE is specified, the <i>pfSave</i> parameter must not be <b>NULL</b>.

The CREDUI_FLAGS_REQUIRE_SMARTCARD and CREDUI_FLAGS_EXCLUDE_CERTIFICATES flags are mutually exclusive. <b>CredUICmdLinePromptForCredentials</b> supports prompting for a smart card certificate or a password-based credential. It does not support certificates that are not smart card certificates or prompting for both on a single call.

Calling Modes

<ul>
<li>The caller will attempt to access the target resource, call credui (passing a description of the target resource and the failure status), call <a href="/windows/desktop/api/wincred/nf-wincred-creduiparseusernamea">CredUIParseUserName</a>, access the target resource again, and then call <a href="/windows/desktop/api/wincred/nf-wincred-creduiconfirmcredentialsa">CredUIConfirmCredentials</a>.</li>
<li>The caller can prompt for credentials without accessing any resources by passing CREDUI_FLAGS_DO_NOT_PERSIST.</li>
</ul>
Target Information

Target Information is  information about the location of the resource to be accessed. For a list of all potential target names for a resource, call 
<a href="/windows/desktop/api/wincred/nf-wincred-credgettargetinfoa">CredGetTargetInfo</a>. <b>CredGetTargetInfo</b> returns information that was cached by the Negotiate, NTLM, or Kerberos authentication package when one of those packages was used to authenticate to the named target. <b>CredGetTargetInfo</b> returns some or all of the following names for the target:

<ul>
<li>NetBIOS server name of the computer</li>
<li>DNS server name of the computer</li>
<li>NetBIOS domain name of the domain the computer belongs to</li>
<li>DNS domain name of the domain the computer belongs to</li>
<li>DNS tree name of the tree the computer belongs to</li>
<li>Name of the package that collected the information</li>
</ul>
 Any piece of this information can be missing if the information does not apply to the target computer. For instance, a computer that is a member of a workgroup does not have a NetBIOS domain name. A computer that is a member of a Windows domain does not have a DNS domain name or DNS tree name.

Credentials are stored in the credential manager based on target name. Each target name is stored as generally as possible without colliding with credentials already stored in the credential manager. An important effect of storing credentials by target name is that a particular user can  have only one credential per target stored in the credential manager.





> [!NOTE]
> The wincred.h header defines CredUICmdLinePromptForCredentials as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/wincred/nf-wincred-credgettargetinfoa">CredGetTargetInfo</a>



<a href="/windows/desktop/api/wincred/nf-wincred-credmarshalcredentiala">CredMarshalCredential</a>



<a href="/windows/desktop/api/wincred/nf-wincred-creduiconfirmcredentialsa">CredUIConfirmCredentials</a>



<a href="/windows/desktop/api/wincred/nf-wincred-creduiparseusernamea">CredUIParseUserName</a>



<a href="/windows/desktop/api/wincred/ns-wincred-credui_infoa">CredUI_INFO</a>



<a href="/windows/desktop/api/winnetwk/nf-winnetwk-wnetaddconnectiona">WNetAddConnection</a>
