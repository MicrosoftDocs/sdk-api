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

# CredRenameA function


## -description


<p class="CCE_Message">[<b>CredRename</b> is no longer supported. Starting with Windows Vista, calls to <b>CredRename</b> always return ERROR_NOT_SUPPORTED.]

The <b>CredRename</b> function renames a credential in the user's credential set. The credential set used is the one associated with the logon session of the current token. The token must not have the user's SID disabled.


## -parameters




### -param OldTargetName [in]

Pointer to a null-terminated string that contains the current name of the credential to be renamed.


### -param NewTargetName [in]

Pointer to a null-terminated string that contains the new name for the credential.


### -param Type [in]

Type of the credential to rename. Must be one of the CRED_TYPE_* defines.


### -param Flags [in]

Flags to control the operation of the function. Currently reserved and must be zero.


## -returns




						The function returns <b>TRUE</b> on success and <b>FALSE</b> on failure. The <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function can be called to get a more specific status code. The following status codes can be returned:

<ul>
<li>ERROR_NOT_FOUND 


There is no credential with the specified <i>OldTargetName</i>.

</li>
<li>ERROR_ALREADY_EXISTS 


There is already a credential or type <i>Type</i> and named <i>NewTargetName</i>.

</li>
<li>ERROR_NO_SUCH_LOGON_SESSION 


The logon session does not exist or there is no credential set associated with this logon session. Network logon sessions do not have an associated credential set.

</li>
<li>ERROR_INVALID_FLAGS 


A flag that is not valid was specified for the <i>Flags</i> parameter.

</li>
</ul>


