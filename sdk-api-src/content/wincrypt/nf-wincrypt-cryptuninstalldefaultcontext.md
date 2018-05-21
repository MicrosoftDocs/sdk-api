---
UID: NF:wincrypt.CryptUninstallDefaultContext
title: CryptUninstallDefaultContext function
author: windows-driver-content
description: Important  This API is deprecated.
old-location: security\cryptuninstalldefaultcontext.htm
old-project: SecCrypto
ms.assetid: ad7be5cf-f078-4a9f-81c4-959e4203dba8
ms.author: windowsdriverdev
ms.date: 5/14/2018
ms.keywords: CryptUninstallDefaultContext, CryptUninstallDefaultContext function [Security], _crypto2_cryptuninstalldefaultcontext, security.cryptuninstalldefaultcontext, wincrypt/CryptUninstallDefaultContext
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: USERNAME_TARGET_CREDENTIAL_INFO, *PUSERNAME_TARGET_CREDENTIAL_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Crypt32.dll
api_name:
-	CryptUninstallDefaultContext
product: Windows
targetos: Windows
req.lib: Crypt32.lib
req.dll: Crypt32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# CryptUninstallDefaultContext function


## -description


<div class="alert"><b>Important</b>  This API is deprecated. New and existing software should start using <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/aa376210%28v=vs.85%29.aspx">Cryptography Next Generation APIs.</a> Microsoft may remove this API in future releases.</div><div> </div>
			The <b>CryptUninstallDefaultContext</b> function removes a default <a href="https://msdn.microsoft.com/library/windows/hardware/hh439393">context</a> previously installed by <a href="https://msdn.microsoft.com/79d121df-0699-424e-a8de-5fc2b396afc2">CryptInstallDefaultContext</a>. This function will block until any threads currently using this context finish, if the default context was installed with CRYPT_DEFAULT_CONTEXT_PROCESS_FLAG set.


## -parameters




### -param hDefaultContext [in]

Handle of the context to be released.


### -param dwFlags [in]

Reserved for future use.


### -param pvReserved [in]

Reserved for future use.


## -returns




						If the function succeeds, the return value is nonzero (TRUE) .If the function fails, the return value is zero (FALSE). For extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.



