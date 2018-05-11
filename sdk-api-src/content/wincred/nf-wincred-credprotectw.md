---
UID: NF:wincred.CredProtectW
title: CredProtectW function
author: windows-driver-content
description: Encrypts the specified credentials so that only the current security context can decrypt them.
old-location: security\credprotect.htm
old-project: SecAuthN
ms.assetid: 1e299dfb-2ffe-463c-9e2c-b7774a2216e3
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: CredProtect, CredProtect function [Security], CredProtectA, CredProtectW, security.credprotect, wincred/CredProtect, wincred/CredProtectA, wincred/CredProtectW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wincred.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CredProtectW (Unicode) and CredProtectA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: CRED_PROTECTION_TYPE, *PCRED_PROTECTION_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Advapi32.dll
-	API-MS-Win-DownLevel-AdvApi32-l2-1-1.dll
-	sechost.dll
-	API-MS-Win-Security-credentials-l1-1-0.dll
api_name:
-	CredProtect
-	CredProtectA
-	CredProtectW
product: Windows
targetos: Windows
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# CredProtectW function


## -description


The <b>CredProtect</b> function encrypts the specified credentials so that only the current security context can decrypt them.


## -parameters




### -param fAsSelf [in]

Set to <b>TRUE</b> to specify that the credentials are encrypted in the security context of the current process. Set to <b>FALSE</b> to specify that credentials are encrypted in the security context of the calling thread security context.


### -param pszCredentials [in]

A pointer to a string that specifies the credentials to encrypt. The function encrypts the number of characters provided in the <i>cchCredentials</i> parameter.


### -param cchCredentials [in]

The size, in characters, of the <i>pszCredentials</i> buffer. 


### -param pszProtectedCredentials [out]

A pointer to a string that, on output, receives the encrypted credentials.


### -param pcchMaxChars [in, out]

The size, in characters of the <i>pszProtectedCredentials</i> buffer. On output, if the <i>pszProtectedCredentials</i> is not of sufficient size to receive the encrypted credentials, this parameter specifies the required size, in characters, of the <i>pszProtectedCredentials</i> buffer.


### -param ProtectionType [out]

A pointer to a <a href="https://msdn.microsoft.com/6d8d8ad6-1b44-4482-a9a2-9c50d522b8d9">CRED_PROTECTION_TYPE</a> enumeration type that, on output, specifies the type of protection provided.


## -returns



<b>TRUE</b> if the function succeeds; otherwise, <b>FALSE</b>.

For extended error information, call the 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function.




## -remarks



Note that the output of the <b>CredProtect</b> function is not integrity protected, so if the output is modified, the <a href="https://msdn.microsoft.com/7a22fb2b-edfc-45f2-b2d2-729f3761584d">CredUnprotect</a> function is not updated and may produce incorrect results.



