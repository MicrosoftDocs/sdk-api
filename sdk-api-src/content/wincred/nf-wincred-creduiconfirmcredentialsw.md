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

# CredUIConfirmCredentialsW function


## -description



			The <b>CredUIConfirmCredentials</b> function is called after 
<a href="https://msdn.microsoft.com/97a8e750-3e63-4e6f-a875-1e5c49c30dd4">CredUIPromptForCredentials</a> or 
<a href="https://msdn.microsoft.com/5b5bfe87-8f31-4228-931e-50cfc399b66b">CredUICmdLinePromptForCredentials</a>, to confirm the validity of the credential harvested. <b>CredUIConfirmCredentials</b> must be called if the CREDUI_FLAGS_EXPECT_CONFIRMATION flag was passed to the "prompt" function, either <a href="https://msdn.microsoft.com/97a8e750-3e63-4e6f-a875-1e5c49c30dd4">CredUIPromptForCredentials</a> or <a href="https://msdn.microsoft.com/5b5bfe87-8f31-4228-931e-50cfc399b66b">CredUICmdLinePromptForCredentials</a>, and the "prompt" function returned NO_ERROR.

After calling the "prompt" function and before calling <b>CredUIConfirmCredentials</b>, the caller must determine whether the credentials are actually valid by using the credentials to access the resource specified by <i>pszTargetName</i>. The results of that validation test are passed to <b>CredUIConfirmCredentials</b> in the <i>bConfirm</i> parameter.


## -parameters




### -param pszTargetName [in]

Pointer to a <b>null</b>-terminated string that contains the name of the target for the credentials, typically a domain or server application name. This must be the same value passed as <i>pszTargetName</i> to <a href="https://msdn.microsoft.com/97a8e750-3e63-4e6f-a875-1e5c49c30dd4">CredUIPromptForCredentials</a> or <a href="https://msdn.microsoft.com/5b5bfe87-8f31-4228-931e-50cfc399b66b">CredUICmdLinePromptForCredentials</a>



### -param bConfirm [in]

Specifies whether the credentials returned from the prompt function are valid. If <b>TRUE</b>, the credentials are stored in the credential manager as defined by <a href="https://msdn.microsoft.com/97a8e750-3e63-4e6f-a875-1e5c49c30dd4">CredUIPromptForCredentials</a> or <a href="https://msdn.microsoft.com/5b5bfe87-8f31-4228-931e-50cfc399b66b">CredUICmdLinePromptForCredentials</a>. If <b>FALSE</b>, the credentials are not stored and various pieces of memory are cleaned up.


## -returns



Status of the operation is returned. The caller can check this status to determine whether the credential confirm operation succeeded. Most applications ignore this status code because the application's connection to the resource has already been done. The operation can fail because the credential was not found on the list of credentials awaiting confirmation, or because the attempt to write or delete the credential failed. Failure to find the credential on the list can occur because the credential was never queued or as a result of too many credentials being queued. Up to five credentials can be queued before older ones are discarded as newer ones are queued.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NO_ERROR - (zero)</b></dt>
</dl>
</td>
<td width="60%">
Confirm operation succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The subject credential could not be found on the confirmation waiting list.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
An attempt to confirm a waiting credential failed because the credential contained data that was not valid or was inconsistent.

</td>
</tr>
</table>
 



