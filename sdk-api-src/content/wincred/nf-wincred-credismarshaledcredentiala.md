---
UID: NF:wincred.CredIsMarshaledCredentialA
title: CredIsMarshaledCredentialA function (wincred.h)
description: Determines whether a specified user name string is a marshaled credential previously marshaled by CredMarshalCredential.
old-location: security\credismarshaledcredential.htm
tech.root: SecAuthN
ms.assetid: fc902c0c-41e0-4178-8ca0-227a1d218388
ms.date: 12/05/2018
ms.keywords: CredIsMarshaledCredential, CredIsMarshaledCredential function [Security], CredIsMarshaledCredentialA, CredIsMarshaledCredentialW, _cred_credismarshaledcredential, security.credismarshaledcredential, wincred/CredIsMarshaledCredential, wincred/CredIsMarshaledCredentialA, wincred/CredIsMarshaledCredentialW
ms.topic: function
f1_keywords:
- wincred/CredIsMarshaledCredential
dev_langs:
- c++
req.header: wincred.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CredIsMarshaledCredentialW (Unicode) and CredIsMarshaledCredentialA (ANSI)
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
- API-MS-Win-DownLevel-AdvApi32-l2-1-1.dll
- sechost.dll
- API-MS-Win-Security-credentials-l1-1-0.dll
api_name:
- CredIsMarshaledCredential
- CredIsMarshaledCredentialA
- CredIsMarshaledCredentialW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CredIsMarshaledCredentialA function


## -description


The <b>CredIsMarshaledCredential</b> function determines whether a specified user name string is a marshaled credential previously marshaled by 
<a href="https://docs.microsoft.com/windows/desktop/api/wincred/nf-wincred-credmarshalcredentiala">CredMarshalCredential</a>.


## -parameters




### -param MarshaledCredential [in]

Pointer to a null-terminated string that contains the marshaled credential.


## -returns



This function returns <b>TRUE</b> if <i>MarshaledCredential</i> is a marshaled credential and <b>FALSE</b> if it is not.



