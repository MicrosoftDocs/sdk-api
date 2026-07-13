---
UID: NF:sspi.SspiPromptForCredentialsA
title: SspiPromptForCredentialsA function (sspi.h)
description: Allows a Security Support Provider Interface (SSPI) application to prompt a user to enter credentials. (ANSI)
helpviewer_keywords: ["SSPIPFC_CREDPROV_DO_NOT_SAVE", "SSPIPFC_NO_CHECKBOX", "SspiPromptForCredentialsA", "sspi/SspiPromptForCredentialsA"]
old-location: security\sspipromptforcredentials.htm
tech.root: security
ms.assetid: 2af2ac00-0e91-4384-9ffa-3e100df218c1
ms.date: 12/05/2018
ms.keywords: SSPIPFC_CREDPROV_DO_NOT_SAVE, SSPIPFC_NO_CHECKBOX, SspiPromptForCredentials, SspiPromptForCredentials function [Security], SspiPromptForCredentialsA, SspiPromptForCredentialsW, security.sspipromptforcredentials, sspi/SspiPromptForCredentials, sspi/SspiPromptForCredentialsA, sspi/SspiPromptForCredentialsW
req.header: sspi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SspiPromptForCredentialsW (Unicode) and SspiPromptForCredentialsA (ANSI)
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
 - SspiPromptForCredentialsA
 - sspi/SspiPromptForCredentialsA
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
 - SspiPromptForCredentials
 - SspiPromptForCredentialsA
 - SspiPromptForCredentialsW
---

# SspiPromptForCredentialsA function


## -description

Allows a <a href="/windows/desktop/SecGloss/s-gly">Security Support Provider Interface </a>(SSPI) application to prompt a user to enter credentials.

## -parameters

### -param pszTargetName [in]

The name of the target to use.

### -param pUiInfo [in]

A pointer to a <a href="/windows/desktop/api/wincred/ns-wincred-credui_infoa">CREDUI_INFO</a> structure that contains information for customizing the appearance of the dialog box that this function displays. 
   


If the <b>hwndParent</b> member of the <a href="/windows/desktop/api/wincred/ns-wincred-credui_infoa">CREDUI_INFO</a> structure is not <b>NULL</b>, this function displays a modal dialog box centered on the parent window.

If the <b>hwndParent</b> member of the <a href="/windows/desktop/api/wincred/ns-wincred-credui_infoa">CREDUI_INFO</a> structure is <b>NULL</b>, the function displays a dialog box centered on the screen.

This function ignores the  <b>hbmBanner</b> member of the <b>CREDUI_INFO</b> structure.

### -param dwAuthError [in]

A Windows error code, defined in Winerror.h, that is displayed in the dialog box. If credentials previously collected were not valid, the caller uses this parameter to pass the error message from the API that collected the credentials (for example, Winlogon) to this function. The corresponding error message is formatted and displayed in the dialog box. Set the  value of this parameter to zero to display no error message.

### -param pszPackage [in]

The name of the security package to use.

### -param pInputAuthIdentity [in]

An identity structure that is used to populate credential fields in the dialog box. To leave the credential fields empty, set the value of this parameter to <b>NULL</b>.

### -param ppAuthIdentity [out]

An identity structure that represents the  credentials this function collects.

When you have finished using this structure, free it by calling the <a href="/windows/desktop/api/sspi/nf-sspi-sspifreeauthidentity">SspiFreeAuthIdentity</a> function.

### -param pfSave [in, out, optional]

A pointer to a Boolean value that, on input, specifies whether the <b>Save</b> check box is selected in the dialog box that this function displays. On output, the value of this parameter specifies whether the <b>Save</b> check box was selected when the user clicked the <b>Submit</b> button in the dialog box. Set this parameter to <b>NULL</b> to ignore the <b>Save</b> check box.

This parameter is ignored if the <b>CREDUIWIN_CHECKBOX</b> flag is not set in the <i>dwFlags</i> parameter.

### -param dwFlags [in]

Flags that determine the behavior of this function. The following flag is currently defined.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SSPIPFC_CREDPROV_DO_NOT_SAVE"></a><a id="sspipfc_credprov_do_not_save"></a><dl>
<dt><b>SSPIPFC_CREDPROV_DO_NOT_SAVE</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
The value of the <i>pfSave</i> parameter is ignored, and the credentials collected by this function are not saved.

<b>Windows 7 and Windows Server 2008 R2:  </b>The value of the <i>pfSave</i> parameter is ignored, and the credentials collected by this function are not saved. Only the name of this possible value was SSPIPFC_SAVE_CRED_BY_CALLER. 

</td>
</tr>
<tr>
<td width="40%"><a id="SSPIPFC_NO_CHECKBOX"></a><a id="sspipfc_no_checkbox"></a><dl>
<dt><b>SSPIPFC_NO_CHECKBOX</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
The value signifies that password and smart card credential providers  will not display the "Remember my credentials" checkbox to the user. The <b>SspiPromptForCredentials</b> function passes this flag value, SSPIPFC_NO_CHECKBOX,  in the <i>pvInAuthBuffer</i> parameter of <a href="/windows/desktop/api/wincred/nf-wincred-creduipromptforwindowscredentialsa">CredUIPromptForWindowsCredentials</a> function.

</td>
</tr>
</table>

## -returns

If the function succeeds, it returns <b>SEC_E_OK</b>.

If the function fails, it returns a nonzero error code.

## -remarks

> [!NOTE]
> The sspi.h header defines SspiPromptForCredentials as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
