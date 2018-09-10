---
UID: NF:wincred.CredUIPromptForWindowsCredentialsW
title: CredUIPromptForWindowsCredentialsW function
author: windows-sdk-content
description: Creates and displays a configurable dialog box that allows users to supply credential information by using any credential provider installed on the local computer.
old-location: security\creduipromptforwindowscredentials.htm
tech.root: SecAuthN
ms.assetid: 946ac279-d30a-4a6c-a76d-d93597121427
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: CREDUIWIN_AUTHPACKAGE_ONLY, CREDUIWIN_CHECKBOX, CREDUIWIN_ENUMERATE_ADMINS, CREDUIWIN_ENUMERATE_CURRENT_USER, CREDUIWIN_GENERIC, CREDUIWIN_IN_CRED_ONLY, CREDUIWIN_PACK_32_WOW, CREDUIWIN_PREPROMPTING, CREDUIWIN_SECURE_PROMPT, CredUIPromptForWindowsCredentials, CredUIPromptForWindowsCredentials function [Security], CredUIPromptForWindowsCredentialsA, CredUIPromptForWindowsCredentialsW, security.creduipromptforwindowscredentials, wincred/CredUIPromptForWindowsCredentials, wincred/CredUIPromptForWindowsCredentialsA, wincred/CredUIPromptForWindowsCredentialsW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wincred.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CredUIPromptForWindowsCredentialsW (Unicode) and CredUIPromptForWindowsCredentialsA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Credui.lib
req.dll: Credui.dll
req.irql: 
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
 - CredUIPromptForWindowsCredentials
 - CredUIPromptForWindowsCredentialsA
 - CredUIPromptForWindowsCredentialsW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CredUIPromptForWindowsCredentialsW function


## -description


The <b>CredUIPromptForWindowsCredentials</b> function creates and displays a configurable dialog box that allows users to supply credential information by using any credential provider installed on the local computer.


## -parameters




### -param pUiInfo [in, optional]

A pointer to a <a href="https://msdn.microsoft.com/b21f8a42-3707-409c-b62a-9bbb29137b9b">CREDUI_INFO</a> structure that contains information for customizing the appearance of the dialog box that this function displays. 
   


If the <b>hwndParent</b> member of the <a href="https://msdn.microsoft.com/b21f8a42-3707-409c-b62a-9bbb29137b9b">CREDUI_INFO</a> structure is not <b>NULL</b>, this function displays a modal dialog box centered on the parent window.

If the <b>hwndParent</b> member of the <a href="https://msdn.microsoft.com/b21f8a42-3707-409c-b62a-9bbb29137b9b">CREDUI_INFO</a> structure is <b>NULL</b>, the function displays a dialog box centered on the screen.

This function ignores the  <b>hbmBanner</b> member of the <b>CREDUI_INFO</b> structure. 


### -param dwAuthError [in]

A Windows error code, defined in Winerror.h, that is displayed in the dialog box. If credentials previously collected were not valid, the caller uses this parameter to pass the error message from the API that collected the credentials (for example, Winlogon) to this function. The corresponding error message is formatted and displayed in the dialog box. Set the  value of this parameter to zero to display no error message.


### -param pulAuthPackage [in, out]

On input, the value of this parameter is used to specify the authentication package for which the credentials in the <i>pvInAuthBuffer</i> buffer are serialized. If the value of <i>pvInAuthBuffer</i> is <b>NULL</b> and the <b>CREDUIWIN_AUTHPACKAGE_ONLY</b> flag is set in the <i>dwFlags</i> parameter, only credential providers capable of serializing credentials for the specified authentication package are to be enumerated. 



To get the appropriate value to use for this parameter on input, call the <a href="https://msdn.microsoft.com/c6504aea-fdba-44ac-b2dc-070707bb1183">LsaLookupAuthenticationPackage</a> function and use the value of the <i>AuthenticationPackage</i> parameter  of that function.

On output, this parameter specifies the authentication package for which the credentials in the <i>ppvOutAuthBuffer</i> buffer are serialized.


### -param pvInAuthBuffer [in, optional]

A pointer to a credential BLOB that is used to populate the credential fields in the dialog box. Set the value of this parameter to <b>NULL</b> to leave the credential fields empty.


### -param ulInAuthBufferSize [in]

The size, in bytes, of the <i>pvInAuthBuffer</i> buffer.


### -param ppvOutAuthBuffer [out]

The address of a pointer that, on output, specifies the credential BLOB. For Kerberos, NTLM, or Negotiate credentials, call the <a href="https://msdn.microsoft.com/c87f0b11-59c2-4450-ad63-398cdb15016f">CredUnPackAuthenticationBuffer</a> function to convert this BLOB to string representations of the credentials.  

When you have finished using the credential BLOB, clear it from memory by calling the <a href="https://msdn.microsoft.com/2c4090a6-025b-4b7b-8f31-7e744ad51b39">SecureZeroMemory</a> function, and free it by calling the <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/ms680722">CoTaskMemFree</a> function.


### -param pulOutAuthBufferSize [out]

The size, in bytes, of the <i>ppvOutAuthBuffer</i> buffer.


### -param pfSave [in, out, optional]

A pointer to a Boolean value that, on input, specifies whether the <b>Save</b> check box is selected in the dialog box that this function displays. On output, the value of this parameter specifies whether the <b>Save</b> check box was selected when the user clicks the <b>Submit</b> button in the dialog box. Set this parameter to <b>NULL</b> to ignore the <b>Save</b> check box.

This parameter is ignored if the <b>CREDUIWIN_CHECKBOX</b> flag is not set in the <i>dwFlags</i> parameter.


### -param dwFlags [in]

A value that specifies behavior for this function. This value can be a bitwise-<b>OR</b> combination of one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CREDUIWIN_GENERIC"></a><a id="creduiwin_generic"></a><dl>
<dt><b>CREDUIWIN_GENERIC</b></dt>
<dt>0x1</dt>
</dl>
</td>
<td width="60%">
The caller is requesting that the credential provider return the user name and password in plain text.

This value cannot be combined with <b>SECURE_PROMPT</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="CREDUIWIN_CHECKBOX"></a><a id="creduiwin_checkbox"></a><dl>
<dt><b>CREDUIWIN_CHECKBOX</b></dt>
<dt>0x2</dt>
</dl>
</td>
<td width="60%">
The <b>Save</b> check box is displayed in the dialog box.

</td>
</tr>
<tr>
<td width="40%"><a id="CREDUIWIN_AUTHPACKAGE_ONLY"></a><a id="creduiwin_authpackage_only"></a><dl>
<dt><b>CREDUIWIN_AUTHPACKAGE_ONLY</b></dt>
<dt>0x10</dt>
</dl>
</td>
<td width="60%">
Only credential providers that support the authentication package specified by the <i>pulAuthPackage</i> parameter should be enumerated.

This value cannot be combined with <b>CREDUIWIN_IN_CRED_ONLY</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="CREDUIWIN_IN_CRED_ONLY"></a><a id="creduiwin_in_cred_only"></a><dl>
<dt><b>CREDUIWIN_IN_CRED_ONLY</b></dt>
<dt>0x20</dt>
</dl>
</td>
<td width="60%">
Only the credentials specified by the <i>pvInAuthBuffer</i> parameter for the authentication package specified by the <i>pulAuthPackage</i> parameter should be enumerated.

If this flag is set, and the <i>pvInAuthBuffer</i> parameter is <b>NULL</b>, the function fails.

This value cannot be combined with <b>CREDUIWIN_AUTHPACKAGE_ONLY</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="CREDUIWIN_ENUMERATE_ADMINS"></a><a id="creduiwin_enumerate_admins"></a><dl>
<dt><b>CREDUIWIN_ENUMERATE_ADMINS</b></dt>
<dt>0x100</dt>
</dl>
</td>
<td width="60%">
Credential providers should enumerate only administrators. This value is intended for User Account Control (UAC) purposes only. We recommend that external callers not set this flag.

</td>
</tr>
<tr>
<td width="40%"><a id="CREDUIWIN_ENUMERATE_CURRENT_USER"></a><a id="creduiwin_enumerate_current_user"></a><dl>
<dt><b>CREDUIWIN_ENUMERATE_CURRENT_USER</b></dt>
<dt>0x200</dt>
</dl>
</td>
<td width="60%">
Only the incoming credentials for the authentication package specified by the <i>pulAuthPackage</i> parameter should be enumerated.

</td>
</tr>
<tr>
<td width="40%"><a id="CREDUIWIN_SECURE_PROMPT"></a><a id="creduiwin_secure_prompt"></a><dl>
<dt><b>CREDUIWIN_SECURE_PROMPT</b></dt>
<dt>0x1000</dt>
</dl>
</td>
<td width="60%">
The credential dialog box should be displayed on the secure desktop. This value cannot be combined with <b>CREDUIWIN_GENERIC</b>.

<b>Windows Vista:  </b>This value is supported beginning with Windows Vista with SP1.

</td>
</tr>
<tr>
<td width="40%"><a id="CREDUIWIN_PREPROMPTING"></a><a id="creduiwin_preprompting"></a><dl>
<dt><b>CREDUIWIN_PREPROMPTING</b></dt>
<dt>0x2000</dt>
</dl>
</td>
<td width="60%">
The credential dialog box is invoked by the <a href="https://msdn.microsoft.com/2af2ac00-0e91-4384-9ffa-3e100df218c1">SspiPromptForCredentials</a> function, and the client is prompted before a prior handshake. If SSPIPFC_NO_CHECKBOX is passed in the <i>pvInAuthBuffer</i> parameter, then the credential provider should not display the check box.

<b>Windows Vista:  </b>This value is supported beginning with Windows Vista with SP1.

</td>
</tr>
<tr>
<td width="40%"><a id="CREDUIWIN_PACK_32_WOW"></a><a id="creduiwin_pack_32_wow"></a><dl>
<dt><b>CREDUIWIN_PACK_32_WOW</b></dt>
<dt>0x10000000</dt>
</dl>
</td>
<td width="60%">
The credential provider should align the credential BLOB pointed to by the <i>ppvOutAuthBuffer</i> parameter to a 32-bit boundary, even if the provider is running on a 64-bit system.

</td>
</tr>
</table>
 


## -returns



If the function succeeds, the function returns <b>ERROR_SUCCESS</b>. If the function is canceled by the user, it returns <b>ERROR_CANCELLED</b>. Any other return value indicates that the function failed to load.




## -remarks



This function does not save credentials.

Applications that use <a href="https://msdn.microsoft.com/91d2389b-1238-49d3-9fef-f1017a8072df">SSPI</a> to authenticate users should not call this function. Instead, call <a href="https://msdn.microsoft.com/2af2ac00-0e91-4384-9ffa-3e100df218c1">SspiPromptForCredentials</a>.



