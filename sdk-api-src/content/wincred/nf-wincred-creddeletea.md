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

# CredDeleteA function


## -description



			The <b>CredDelete</b> function deletes a credential from the user's credential set. The credential set used is the one associated with the logon session of the current token. The token must not have the user's SID disabled.


## -parameters




### -param TargetName [in]

Pointer to a null-terminated string that contains the name of the credential to delete.


### -param Type [in]

Type of the credential to delete. Must be one of the CRED_TYPE_* defined types. For a list of the defined types, see the <b>Type</b> member of the <a href="https://msdn.microsoft.com/6361b93c-4441-4a01-bd39-b95c42962497">CREDENTIAL</a> structure.

If the value of this parameter is <b>CRED_TYPE_DOMAIN_EXTENDED</b>, this function can delete a credential that specifies a user name when there are multiple credentials for the same target. The value of the <i>TargetName</i> parameter must specify the user name as <i>Target</i><b>|</b><i>UserName</i>.


### -param Flags [in]

Reserved and must be zero.


## -returns




						The function returns <b>TRUE</b> on success and <b>FALSE</b> on failure. The <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function can be called to get a more specific status code. The following status codes can be returned:
						

<ul>
<li>ERROR_NOT_FOUND 


There is no credential with the specified <i>TargetName</i>.
								

</li>
<li>ERROR_NO_SUCH_LOGON_SESSION 


The logon session does not exist or there is no credential set associated with this logon session. Network logon sessions do not have an associated credential set.

</li>
<li>ERROR_INVALID_FLAGS 


A flag that is not valid was specified for the <i>Flags</i> parameter.

</li>
</ul>


