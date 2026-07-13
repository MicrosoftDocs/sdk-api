---
UID: NF:wincred.CredUIPromptForCredentialsA
title: CredUIPromptForCredentialsA function (wincred.h)
description: Creates and displays a configurable dialog box that accepts credentials information from a user. (ANSI)
helpviewer_keywords: ["CREDUI_FLAGS_ALWAYS_SHOW_UI", "CREDUI_FLAGS_COMPLETE_USERNAME", "CREDUI_FLAGS_DO_NOT_PERSIST", "CREDUI_FLAGS_EXCLUDE_CERTIFICATES", "CREDUI_FLAGS_EXPECT_CONFIRMATION", "CREDUI_FLAGS_GENERIC_CREDENTIALS", "CREDUI_FLAGS_INCORRECT_PASSWORD", "CREDUI_FLAGS_KEEP_USERNAME", "CREDUI_FLAGS_PASSWORD_ONLY_OK", "CREDUI_FLAGS_PERSIST", "CREDUI_FLAGS_REQUEST_ADMINISTRATOR", "CREDUI_FLAGS_REQUIRE_CERTIFICATE", "CREDUI_FLAGS_REQUIRE_SMARTCARD", "CREDUI_FLAGS_SERVER_CREDENTIAL", "CREDUI_FLAGS_SHOW_SAVE_CHECK_BOX", "CREDUI_FLAGS_USERNAME_TARGET_CREDENTIALS", "CREDUI_FLAGS_VALIDATE_USERNAME", "CredUIPromptForCredentialsA", "wincred/CredUIPromptForCredentialsA"]
old-location: security\creduipromptforcredentials.htm
tech.root: security
ms.assetid: 97a8e750-3e63-4e6f-a875-1e5c49c30dd4
ms.date: 12/05/2018
ms.keywords: CREDUI_FLAGS_ALWAYS_SHOW_UI, CREDUI_FLAGS_COMPLETE_USERNAME, CREDUI_FLAGS_DO_NOT_PERSIST, CREDUI_FLAGS_EXCLUDE_CERTIFICATES, CREDUI_FLAGS_EXPECT_CONFIRMATION, CREDUI_FLAGS_GENERIC_CREDENTIALS, CREDUI_FLAGS_INCORRECT_PASSWORD, CREDUI_FLAGS_KEEP_USERNAME, CREDUI_FLAGS_PASSWORD_ONLY_OK, CREDUI_FLAGS_PERSIST, CREDUI_FLAGS_REQUEST_ADMINISTRATOR, CREDUI_FLAGS_REQUIRE_CERTIFICATE, CREDUI_FLAGS_REQUIRE_SMARTCARD, CREDUI_FLAGS_SERVER_CREDENTIAL, CREDUI_FLAGS_SHOW_SAVE_CHECK_BOX, CREDUI_FLAGS_USERNAME_TARGET_CREDENTIALS, CREDUI_FLAGS_VALIDATE_USERNAME, CredUIPromptForCredentials, CredUIPromptForCredentials function [Security], CredUIPromptForCredentialsA, CredUIPromptForCredentialsW, _cred_creduipromptforcredentials, security.creduipromptforcredentials, wincred/CredUIPromptForCredentials, wincred/CredUIPromptForCredentialsA, wincred/CredUIPromptForCredentialsW
req.header: wincred.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CredUIPromptForCredentialsW (Unicode) and CredUIPromptForCredentialsA (ANSI)
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
 - CredUIPromptForCredentialsA
 - wincred/CredUIPromptForCredentialsA
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
 - CredUIPromptForCredentials
 - CredUIPromptForCredentialsA
 - CredUIPromptForCredentialsW
---

# CredUIPromptForCredentialsA function


## -description

The <b>CredUIPromptForCredentials</b> function creates and displays a configurable dialog box that accepts credentials information from a user.

Applications that target Windows Vista or Windows Server 2008 should call <a href="/windows/desktop/api/wincred/nf-wincred-creduipromptforwindowscredentialsa">CredUIPromptForWindowsCredentials</a> instead of this function, for the following reasons:<ul>
<li>
<a href="/windows/desktop/api/wincred/nf-wincred-creduipromptforwindowscredentialsa">CredUIPromptForWindowsCredentials</a> is consistent with the current Windows user interface.</li>
<li>
<a href="/windows/desktop/api/wincred/nf-wincred-creduipromptforwindowscredentialsa">CredUIPromptForWindowsCredentials</a> is more extensible, allowing integration of additional authentication mechanisms such as biometrics and smart cards.</li>
<li>
<a href="/windows/desktop/api/wincred/nf-wincred-creduipromptforwindowscredentialsa">CredUIPromptForWindowsCredentials</a> is compliant with the Common Criteria specification.</li>
</ul>

## -parameters

### -param pUiInfo [in, optional]

A pointer to a <a href="/windows/desktop/api/wincred/ns-wincred-credui_infoa">CREDUI_INFO</a> structure that contains information for customizing the appearance of the dialog box.

### -param pszTargetName [in]

A pointer to a null-terminated string that contains  the name of the target for the credentials, typically a server name. For Distributed File System (DFS) connections, this string is of the form <i>ServerName</i>&#92;<i>ShareName</i>. This parameter is used to identify target information when storing and retrieving credentials.

### -param pContext [in]

This parameter is reserved for future use. It must be <b>NULL</b>.

### -param dwAuthError [in, optional]

Specifies why the credential dialog box is needed. A caller can pass this Windows error parameter, returned by another authentication call, to allow the dialog box to accommodate certain errors. For example, if the password expired status code is passed, the dialog box could prompt the user to change the password on the account.

### -param pszUserName [in, out]

A pointer to a null-terminated string that contains the user name for the credentials. If a nonzero-length string is passed, the <i>UserName</i> option of the dialog box is prefilled with the string. In the case of credentials other than <i>UserName</i>/<i>Password</i>, a marshaled format of the credential can be passed in. This string is created by calling 
<a href="/windows/desktop/api/wincred/nf-wincred-credmarshalcredentiala">CredMarshalCredential</a>.

This function copies the user-supplied name to this buffer, copying a maximum of <i>ulUserNameMaxChars</i> characters. This format can be converted to <i>UserName</i>/<i>Password</i> format by using 
<a href="/windows/desktop/api/wincred/nf-wincred-creduiparseusernamea">CredUIParseUsername</a>. A marshaled format can be passed directly to a <a href="/windows/desktop/SecGloss/s-gly">security support provider</a> (SSP).

If the CREDUI_FLAGS_DO_NOT_PERSIST flag is not specified, the value returned in this parameter is of a form that should not be inspected, printed, or persisted other than passing it to <a href="/windows/desktop/api/wincred/nf-wincred-creduiparseusernamea">CredUIParseUsername</a>. The subsequent results of <b>CredUIParseUsername</b> can  be passed only to a client-side authentication function such as <a href="/windows/desktop/api/winnetwk/nf-winnetwk-wnetaddconnectiona">WNetAddConnection</a> or an SSP function.

If no domain or server is specified as part of this parameter, the value of the  <b>pszTargetName</b> parameter is used as the domain to form a <i>DomainName</i>&#92;<i>UserName</i> pair. On output, this parameter receives a string that contains that <i>DomainName</i>&#92;<i>UserName</i> pair.

### -param ulUserNameBufferSize [in]

The maximum number of characters that can be copied to <i>pszUserName</i> including the terminating null character.

<div class="alert"><b>Note</b>  CREDUI_MAX_USERNAME_LENGTH does not include the terminating null character.</div>
<div> </div>

### -param pszPassword [in, out]

A pointer to a null-terminated string that contains the password for the credentials. If a nonzero-length string is specified for <i>pszPassword</i>, the password option of the dialog box will be prefilled with the string.

This function copies the user-supplied password to this buffer, copying a maximum of <i>ulPasswordMaxChars</i> characters. If the CREDUI_FLAGS_DO_NOT_PERSIST flag is not specified, the value returned in this parameter is of a form that should not be inspected, printed, or persisted other than passing it to a client-side authentication function such as <a href="/windows/desktop/api/winnetwk/nf-winnetwk-wnetaddconnectiona">WNetAddConnection</a> or an SSP function.

When you have finished using the password, clear the password from memory by calling the <a href="/previous-versions/windows/desktop/legacy/aa366877(v=vs.85)">SecureZeroMemory</a> function. For more information about protecting passwords, see <a href="/windows/desktop/SecBP/handling-passwords">Handling Passwords</a>.

### -param ulPasswordBufferSize [in]

The maximum number of characters that can be copied to <i>pszPassword</i> including the terminating null character.

<div class="alert"><b>Note</b>  CREDUI_MAX_PASSWORD_LENGTH does not include the terminating null character.</div>
<div> </div>

### -param save [in, out]

A pointer to a <b>BOOL</b> that specifies the initial state of the <b>Save</b> check box and receives the state of the <b>Save</b> check box after the user has responded to the dialog box. If this value is not <b>NULL</b>  and <b>CredUIPromptForCredentials</b> returns NO_ERROR, then <i>pfSave</i> returns the state of the <b>Save</b> check box when the user chose <b>OK</b> in the dialog box.

If the CREDUI_FLAGS_PERSIST flag is specified, the <b>Save</b> check box is not displayed, but is considered to be selected.

If the CREDUI_FLAGS_DO_NOT_PERSIST flag is specified and CREDUI_FLAGS_SHOW_SAVE_CHECK_BOX is not specified, the <b>Save</b> check box is not displayed, but is considered to be cleared.

An application that needs to use CredUI to prompt the user for credentials, but does not need the credential management services provided by the credential manager, can use <i>pfSave</i> to receive the state of the <b>Save</b> check box after the user closes the dialog box. To do this, the caller must specify CREDUI_FLAGS_DO_NOT_PERSIST and  CREDUI_FLAGS_SHOW_SAVE_CHECK_BOX in <i>dwFlags</i>. When CREDUI_FLAGS_DO_NOT_PERSIST and  CREDUI_FLAGS_SHOW_SAVE_CHECK_BOX are set, the application is responsible for examining *<i>pfSave</i> after the function returns, and if *<i>pfSave</i> is <b>TRUE</b>,  then the application must take the appropriate action to save the user credentials within the resources of the application.

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
<dt>0x00080</dt>
</dl>
</td>
<td width="60%">
Specifies that a user interface will be shown even if the credentials can be returned from an existing credential in credential manager. This flag is  permitted only if CREDUI_FLAGS_GENERIC_CREDENTIALS is also specified.

</td>
</tr>
<tr>
<td width="40%"><a id="CREDUI_FLAGS_COMPLETE_USERNAME"></a><a id="credui_flags_complete_username"></a><dl>
<dt><b>CREDUI_FLAGS_COMPLETE_USERNAME</b></dt>
<dt>0x00800</dt>
</dl>
</td>
<td width="60%">
Populate the combo box with the prompt for a user name.

</td>
</tr>
<tr>
<td width="40%"><a id="CREDUI_FLAGS_DO_NOT_PERSIST"></a><a id="credui_flags_do_not_persist"></a><dl>
<dt><b>CREDUI_FLAGS_DO_NOT_PERSIST</b></dt>
<dt>0x00002</dt>
</dl>
</td>
<td width="60%">
Do not store credentials or display check boxes. You can pass CREDUI_FLAGS_SHOW_SAVE_CHECK_BOX with this flag to display the <b>Save</b> check box only, and the result is returned in the <i>pfSave</i> output parameter.

</td>
</tr>
<tr>
<td width="40%"><a id="CREDUI_FLAGS_EXCLUDE_CERTIFICATES"></a><a id="credui_flags_exclude_certificates"></a><dl>
<dt><b>CREDUI_FLAGS_EXCLUDE_CERTIFICATES</b></dt>
<dt>0x00008</dt>
</dl>
</td>
<td width="60%">
Populate the combo box with user name/password only. Do not display certificates or smart cards in the combo box.

</td>
</tr>
<tr>
<td width="40%"><a id="CREDUI_FLAGS_EXPECT_CONFIRMATION"></a><a id="credui_flags_expect_confirmation"></a><dl>
<dt><b>CREDUI_FLAGS_EXPECT_CONFIRMATION</b></dt>
<dt>0x20000</dt>
</dl>
</td>
<td width="60%">
Specifies that the caller will call <a href="/windows/desktop/api/wincred/nf-wincred-creduiconfirmcredentialsa">CredUIConfirmCredentials</a> after checking to determine whether the returned credentials are actually valid. This mechanism ensures that credentials that are not valid are not saved to the credential manager. Specify this flag in all cases unless CREDUI_FLAGS_DO_NOT_PERSIST is specified.

</td>
</tr>
<tr>
<td width="40%"><a id="CREDUI_FLAGS_GENERIC_CREDENTIALS"></a><a id="credui_flags_generic_credentials"></a><dl>
<dt><b>CREDUI_FLAGS_GENERIC_CREDENTIALS</b></dt>
<dt>0x40000</dt>
</dl>
</td>
<td width="60%">
Consider the credentials entered by the user to be generic credentials.

</td>
</tr>
<tr>
<td width="40%"><a id="CREDUI_FLAGS_INCORRECT_PASSWORD"></a><a id="credui_flags_incorrect_password"></a><dl>
<dt><b>CREDUI_FLAGS_INCORRECT_PASSWORD</b></dt>
<dt>0x00001</dt>
</dl>
</td>
<td width="60%">
Notify the user of insufficient credentials by displaying the "Logon unsuccessful" balloon tip.

</td>
</tr>
<tr>
<td width="40%"><a id="CREDUI_FLAGS_KEEP_USERNAME"></a><a id="credui_flags_keep_username"></a><dl>
<dt><b>CREDUI_FLAGS_KEEP_USERNAME</b></dt>
<dt>0x100000</dt>
</dl>
</td>
<td width="60%">
Do not allow the user to change the supplied user name.

</td>
</tr>
<tr>
<td width="40%"><a id="CREDUI_FLAGS_PASSWORD_ONLY_OK"></a><a id="credui_flags_password_only_ok"></a><dl>
<dt><b>CREDUI_FLAGS_PASSWORD_ONLY_OK</b></dt>
<dt>0x00200</dt>
</dl>
</td>
<td width="60%">
Populate the combo box with the password only. Do not allow a user name to be entered.

</td>
</tr>
<tr>
<td width="40%"><a id="CREDUI_FLAGS_PERSIST"></a><a id="credui_flags_persist"></a><dl>
<dt><b>CREDUI_FLAGS_PERSIST</b></dt>
<dt>0x01000</dt>
</dl>
</td>
<td width="60%">
Do not show the <b>Save</b> check box, but the credential is saved as though the box were shown and selected.

</td>
</tr>
<tr>
<td width="40%"><a id="CREDUI_FLAGS_REQUEST_ADMINISTRATOR"></a><a id="credui_flags_request_administrator"></a><dl>
<dt><b>CREDUI_FLAGS_REQUEST_ADMINISTRATOR</b></dt>
<dt>0x00004</dt>
</dl>
</td>
<td width="60%">
Populate the combo box with local administrators only.<b>Windows XP Home Edition:  </b>This flag will filter out the well-known Administrator account.



</td>
</tr>
<tr>
<td width="40%"><a id="CREDUI_FLAGS_REQUIRE_CERTIFICATE"></a><a id="credui_flags_require_certificate"></a><dl>
<dt><b>CREDUI_FLAGS_REQUIRE_CERTIFICATE</b></dt>
<dt>0x00010</dt>
</dl>
</td>
<td width="60%">
Populate the combo box with certificates and smart cards only. Do not allow a user name to be entered.

</td>
</tr>
<tr>
<td width="40%"><a id="CREDUI_FLAGS_REQUIRE_SMARTCARD"></a><a id="credui_flags_require_smartcard"></a><dl>
<dt><b>CREDUI_FLAGS_REQUIRE_SMARTCARD</b></dt>
<dt>0x00100</dt>
</dl>
</td>
<td width="60%">
Populate the combo box with certificates or smart cards only. Do not allow a user name to be entered.

</td>
</tr>
<tr>
<td width="40%"><a id="CREDUI_FLAGS_SERVER_CREDENTIAL"></a><a id="credui_flags_server_credential"></a><dl>
<dt><b>CREDUI_FLAGS_SERVER_CREDENTIAL</b></dt>
<dt>0x04000</dt>
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
<dt>0x00040</dt>
</dl>
</td>
<td width="60%">
If the check box is selected, show the <b>Save</b> check box and return <b>TRUE</b> in the <i>pfSave</i> output parameter, otherwise, return <b>FALSE</b>. Check box uses the value in <i>pfSave</i> by default.

</td>
</tr>
<tr>
<td width="40%"><a id="CREDUI_FLAGS_USERNAME_TARGET_CREDENTIALS"></a><a id="credui_flags_username_target_credentials"></a><dl>
<dt><b>CREDUI_FLAGS_USERNAME_TARGET_CREDENTIALS</b></dt>
<dt>0x80000</dt>
</dl>
</td>
<td width="60%">
The credential is a "runas" credential. The <i>TargetName</i> parameter specifies the name of the command or program being run. It is used for prompting purposes only.

</td>
</tr>
<tr>
<td width="40%"><a id="CREDUI_FLAGS_VALIDATE_USERNAME"></a><a id="credui_flags_validate_username"></a><dl>
<dt><b>CREDUI_FLAGS_VALIDATE_USERNAME</b></dt>
<dt>0x00400</dt>
</dl>
</td>
<td width="60%">
Check that the user name is valid.

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
<dt><b>ERROR_CANCELLED</b></dt>
</dl>
</td>
<td width="60%">
User chose <b>Cancel</b>. The <i>pszUserName</i> and <i>pszPassword</i> parameters have not changed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_FLAGS</b></dt>
</dl>
</td>
<td width="60%">
This status is returned for any of the flag configurations that are not valid.

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
The credential manager cannot be used. Typically, this error is handled by calling <a href="/windows/desktop/api/wincred/nf-wincred-creduipromptforcredentialsa">CredUIPromptForCredentials</a> and passing in the CREDUI_FLAGS_DO_NOT_PERSIST flag.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NO_ERROR</b></dt>
</dl>
</td>
<td width="60%">
User chose <b>OK</b>. The  <i>pszUserName</i>, <i>pszPassword</i>, and <i>pfSave</i> parameters will return the values documented earlier.

</td>
</tr>
</table>

## -remarks

The <b>CredUIPromptForCredentials</b> function creates and displays an application modal dialog box. After the dialog box is displayed and until it is closed by the user or application, no other window in the application can become active.

The flags CREDUI_FLAGS_REQUIRE_SMARTCARD, CREDUI_FLAGS_REQUIRE_CERTIFICATE, and CREDUI_FLAGS_EXCLUDE_CERTIFICATE are mutually exclusive.

If CREDUI_FLAGS_DO_NOT_PERSIST is specified, either <i>pszTargetName</i> must be specified or <i>uiInfo-&gt;pszMessageText</i> and <i>uiInfo-&gt;pszCaption</i> must be specified.

The flags CREDUI_FLAG_USERNAME_TARGET_CREDENTIALS and CREDUI_FLAGS_GENERIC_CREDENTIALS are mutually exclusive. If neither is specified, the credential is a domain credential.

An X509 certificate must have an <a href="/windows/desktop/SecGloss/e-gly">enhanced key usage</a> (EKU) value of <b>szOID_KP_SMARTCARD_LOGON</b> (1.3.6.1.4.1.311.20.2.2) to be displayed.

<b>Windows XP:  </b>This EKU value is not required to display X509 certificates.

If CREDUI_FLAGS_GENERIC_CREDENTIALS is not specified or CREDUI_FLAGS_COMPLETE_USERNAME is specified, the typed name is <i>syntax checked</i>. Syntax checking applies the same rules as applied by <a href="/windows/desktop/api/wincred/nf-wincred-creduiparseusernamea">CredUIParseUserName</a>. If the typed name is not valid, the user is prompted for a valid one. If the domain portion of the typed name is missing, one will be supplied based on the target name.

If CREDUI_FLAGS_GENERIC_CREDENTIALS is specified and CREDUI_FLAGS_VALIDATE_USERNAME is also specified, the typed name is syntax checked. If the typed name is not valid, the user is prompted for a valid one.

If CREDUI_FLAGS_GENERIC_CREDENTIALS is specified and neither CREDUI_FLAGS_COMPLETE_USERNAME nor CREDUI_FLAGS_VALIDATE_USERNAME is specified, the typed name is not syntax checked in any way.

If neither CREDUI_FLAGS_PERSIST nor CREDUI_FLAGS_DO_NOT_PERSIST is set, the <b>Save</b> check box is shown, and it controls whether the credential is saved.

Calling Modes

<ul>
<li>The caller will attempt to access the target resource, call credui (passing a description of the target resource and the failure status), call <a href="/windows/desktop/api/wincred/nf-wincred-creduiparseusernamea">CredUIParseUserName</a>, access the target resource again, and then call <a href="/windows/desktop/api/wincred/nf-wincred-creduiconfirmcredentialsa">CredUIConfirmCredentials</a>.</li>
<li>The caller can prompt for credentials without accessing any resources by passing CREDUI_FLAGS_DO_NOT_PERSIST.</li>
<li>For generic credentials, there is no authentication package. Therefore, the application needs to access the credential to do the authentication. Prompt for credentials, not passing CREDUI_FLAGS_ALWAYS_SHOW_UI before the first authentication. The user interface will appear only if there is no credential in the credential manager. On all subsequent messages from within the application, CREDUI_FLAGS_ALWAYS_SHOW_UI will be passed because the credential in the credential manager is clearly not valid for that resource.</li>
</ul>
Target Information

Target Information is  information about the location of the resource to be accessed. For a list of all potential target names for a resource, call 
<a href="/windows/desktop/api/wincred/nf-wincred-credgettargetinfoa">CredGetTargetInfo</a>. <b>CredGetTargetInfo</b> returns information that was cached by the Negotiate, NTLM, or Kerberos authentication package when one of those packages was used to authenticate to the named target. <b>CredGetTargetInfo</b> returns some or all of the following names for the target:

<ul>
<li>NetBIOS server name of the computer </li>
<li>DNS server name of the computer</li>
<li>NetBIOS domain name of the domain the computer belongs to</li>
<li>DNS domain name of the domain the computer belongs to</li>
<li>DNS tree name of the tree the computer belongs to</li>
<li>Name of the package that collected the information</li>
</ul>
Any piece of this information can be missing if the information does not apply to the target computer. For instance, a computer that is a member of a workgroup does not have a NetBIOS domain name.

Credentials are stored in the credential manager based on target name. Each target name is stored as generally as possible without colliding with credentials already stored in the credential manager. Because credentials are stored by target name, a particular user can only have one credential per target stored in the credential manager.





> [!NOTE]
> The wincred.h header defines CredUIPromptForCredentials as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/wincred/nf-wincred-credgettargetinfoa">CredGetTargetInfo</a>



<a href="/windows/desktop/api/wincred/nf-wincred-credmarshalcredentiala">CredMarshalCredential</a>



<a href="/windows/desktop/api/wincred/nf-wincred-creduiconfirmcredentialsa">CredUIConfirmCredentials</a>



<a href="/windows/desktop/api/wincred/nf-wincred-creduiparseusernamea">CredUIParseUserName</a>



<a href="/windows/desktop/api/wincred/nf-wincred-creduipromptforwindowscredentialsa">CredUIPromptForWindowsCredentials</a>



<a href="/windows/desktop/api/wincred/ns-wincred-credui_infoa">CredUI_INFO</a>



<a href="/windows/desktop/api/winnetwk/nf-winnetwk-wnetaddconnectiona">WNetAddConnection</a>
