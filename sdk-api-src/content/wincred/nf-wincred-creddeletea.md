---
UID: NF:wincred.CredDeleteA
title: CredDeleteA function (wincred.h)
description: Deletes a credential from the user's credential set. (ANSI)
helpviewer_keywords: ["CredDeleteA", "wincred/CredDeleteA"]
old-location: security\creddelete.htm
tech.root: security
ms.assetid: 154af9c8-18fd-412d-899d-7c6d2138380d
ms.date: 12/05/2018
ms.keywords: CredDelete, CredDelete function [Security], CredDeleteA, CredDeleteW, _cred_creddelete, security.creddelete, wincred/CredDelete, wincred/CredDeleteA, wincred/CredDeleteW
req.header: wincred.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CredDeleteW (Unicode) and CredDeleteA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CredDeleteA
 - wincred/CredDeleteA
dev_langs:
 - c++
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
 - CredDelete
 - CredDeleteA
 - CredDeleteW
---

# CredDeleteA function


## -description

The <b>CredDelete</b> function deletes a credential from the user's credential set. The credential set used is the one associated with the logon session of the current token. The token must not have the user's SID disabled.

## -parameters

### -param TargetName [in]

Pointer to a null-terminated string that contains the name of the credential to delete.

### -param Type [in]

Type of the credential to delete. Must be one of the CRED_TYPE_* defined types. For a list of the defined types, see the <b>Type</b> member of the <a href="/windows/desktop/api/wincred/ns-wincred-credentiala">CREDENTIAL</a> structure.

If the value of this parameter is <b>CRED_TYPE_DOMAIN_EXTENDED</b>, this function can delete a credential that specifies a user name when there are multiple credentials for the same target. The value of the <i>TargetName</i> parameter must specify the user name as <i>Target</i><b>|</b><i>UserName</i>.

### -param Flags [in]

Reserved and must be zero.

## -returns

The function returns <b>TRUE</b> on success and <b>FALSE</b> on failure. The <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function can be called to get a more specific status code. The following status codes can be returned:
						

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

## -remarks

> [!NOTE]
> The wincred.h header defines CredDelete as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
