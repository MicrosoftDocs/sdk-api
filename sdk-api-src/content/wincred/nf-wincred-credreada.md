---
UID: NF:wincred.CredReadA
title: CredReadA function (wincred.h)
description: Reads a credential from the user's credential set. (ANSI)
helpviewer_keywords: ["CredReadA", "wincred/CredReadA"]
old-location: security\credread.htm
tech.root: security
ms.assetid: 3222de7b-5290-4e82-a382-b2db6afc78cc
ms.date: 12/05/2018
ms.keywords: CredRead, CredRead function [Security], CredReadA, CredReadW, _cred_credread, security.credread, wincred/CredRead, wincred/CredReadA, wincred/CredReadW
req.header: wincred.h
req.include-header: 
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
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CredReadA
 - wincred/CredReadA
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
 - CredRead
 - CredReadA
 - CredReadW
---

# CredReadA function


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
Any pointers contained within the buffer are pointers to locations within this single allocated block. The single returned buffer must be freed by calling <a href="/windows/desktop/api/wincred/nf-wincred-credfree">CredFree</a>.

## -returns

The function returns <b>TRUE</b> on success and <b>FALSE</b> on failure. The <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function can be called to get a more specific status code. The following status codes can be returned:

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

If the value of the <b>Type</b> member of the <a href="/windows/desktop/api/wincred/ns-wincred-credentiala">CREDENTIAL</a> structure specified by the <i>Credential</i>  parameter is <b>CRED_TYPE_DOMAIN_EXTENDED</b>, a namespace must be specified in the target name. This function can return only one credential of the specified type.




> [!NOTE]
> The wincred.h header defines CredRead as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
