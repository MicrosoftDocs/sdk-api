---
UID: NF:wincred.CredReadW
title: CredReadW function
author: windows-sdk-content
description: Reads a credential from the user's credential set.
old-location: security\credread.htm
old-project: secauthn
ms.assetid: 3222de7b-5290-4e82-a382-b2db6afc78cc
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: CredRead, CredRead function [Security], CredReadA, CredReadW, _cred_credread, security.credread, wincred/CredRead, wincred/CredReadA, wincred/CredReadW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: wincred.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CredReadW (Unicode) and CredReadA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: CRED_PROTECTION_TYPE, *PCRED_PROTECTION_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Advapi32.dll
 - API-MS-Win-DownLevel-AdvApi32-l2-1-0.dll
 - sechost.dll
 - API-MS-Win-DownLevel-AdvApi32-l2-1-1.dll
 - API-MS-Win-Security-credentials-l1-1-0.dll
api_name:
 - CredRead
 - CredReadA
 - CredReadW
product: Windows
targetos: Windows
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# CredReadW function


## -description


The <b>CredRead</b> function reads a credential from the user's credential set. The credential set used is the one associated with the logon session of the current token. The token must not have the user's SID disabled.


## -parameters




### -param TargetName [in]

Pointer to a null-terminated string that contains the name of the credential to read.


### -param Type [in]

Type of the credential to read. <i>Type</i> must be one of the CRED_TYPE_* defined types.


### -param Flags [in]

Currently reserved and must be zero.


### -param Credential [out]

Pointer to a single allocated block buffer to return the credential.
Any pointers contained within the buffer are pointers to locations within this single allocated block. The single returned buffer must be freed by calling <a href="https://msdn.microsoft.com/bc33ab1b-dd3f-4e1b-96d2-e32ceff89ada">CredFree</a>.


## -returns



The function returns <b>TRUE</b> on success and <b>FALSE</b> on failure. The <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function can be called to get a more specific status code. The following status codes can be returned:

<ul>
<li>ERROR_NOT_FOUND 


No credential exists with the specified <i>TargetName</i>.
								

</li>
<li>ERROR_NO_SUCH_LOGON_SESSION 


The logon session does not exist or there is no credential set associated with this logon session. Network logon sessions do not have an associated credential set.

</li>
<li>ERROR_INVALID_FLAGS 


A flag that is not valid was specified for the <i>Flags</i> parameter.

</li>
</ul>



## -remarks



If the value of the <b>Type</b> member of the <a href="https://msdn.microsoft.com/6361b93c-4441-4a01-bd39-b95c42962497">CREDENTIAL</a> structure specified by the <i>Credential</i>  parameter is <b>CRED_TYPE_DOMAIN_EXTENDED</b>, a namespace must be specified in the target name. This function can return only one credential of the specified type.



