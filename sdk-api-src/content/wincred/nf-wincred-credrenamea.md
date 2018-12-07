---
UID: NF:wincred.CredRenameA
title: CredRenameA function
author: windows-sdk-content
description: CredRename is no longer supported.
old-location: security\credrename.htm
tech.root: secauthn
ms.assetid: e598f2ae-f975-4dd2-bf0b-e2fd96d4c940
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CredRename, CredRename function [Security], CredRenameA, CredRenameW, _cred_credrename, security.credrename, wincred/CredRename, wincred/CredRenameA, wincred/CredRenameW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wincred.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CredRenameW (Unicode) and CredRenameA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Advapi32.dll
api_name:
 - CredRename
 - CredRenameA
 - CredRenameW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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


