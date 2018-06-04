---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# SspiPromptForCredentialsA function


## -description


Allows a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">Security Support Provider Interface </a>(SSPI) application to prompt a user to enter credentials.


## -parameters




### -param pszTargetName [in]

The name of the target to use.


### -param pUiInfo [in]

A pointer to a <a href="https://msdn.microsoft.com/b21f8a42-3707-409c-b62a-9bbb29137b9b">CREDUI_INFO</a> structure that contains information for customizing the appearance of the dialog box that this function displays. 
   


If the <b>hwndParent</b> member of the <a href="https://msdn.microsoft.com/b21f8a42-3707-409c-b62a-9bbb29137b9b">CREDUI_INFO</a> structure is not <b>NULL</b>, this function displays a modal dialog box centered on the parent window.

If the <b>hwndParent</b> member of the <a href="https://msdn.microsoft.com/b21f8a42-3707-409c-b62a-9bbb29137b9b">CREDUI_INFO</a> structure is <b>NULL</b>, the function displays a dialog box centered on the screen.

This function ignores the  <b>hbmBanner</b> member of the <b>CREDUI_INFO</b> structure. 


### -param dwAuthError [in]

A Windows error code, defined in Winerror.h, that is displayed in the dialog box. If credentials previously collected were not valid, the caller uses this parameter to pass the error message from the API that collected the credentials (for example, Winlogon) to this function. The corresponding error message is formatted and displayed in the dialog box. Set the  value of this parameter to zero to display no error message.


### -param pszPackage [in]

The name of the security package to use.


### -param pInputAuthIdentity [in]

An identity structure that is used to populate credential fields in the dialog box. To leave the credential fields empty, set the value of this parameter to <b>NULL</b>.


### -param ppAuthIdentity [out]

An identity structure that represents the  credentials this function collects.

When you have finished using this structure, free it by calling the <a href="https://msdn.microsoft.com/6199f66e-7adb-4bb9-8e77-a735e31dd5f6">SspiFreeAuthIdentity</a> function.


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
The value signifies that password and smart card credential providers  will not display the "Remember my credentials" checkbox to the user. The <b>SspiPromptForCredentials</b> function passes this flag value, SSPIPFC_NO_CHECKBOX,  in the <i>pvInAuthBuffer</i> parameter of <a href="https://msdn.microsoft.com/946ac279-d30a-4a6c-a76d-d93597121427">CredUIPromptForWindowsCredentials</a> function.

</td>
</tr>
</table>
 


## -returns




						If the function succeeds, it returns <b>SEC_E_OK</b>.

If the function fails, it returns a nonzero error code.



