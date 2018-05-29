---
UID: NF:sspi.ChangeAccountPasswordA
title: ChangeAccountPasswordA function
author: windows-sdk-content
description: Changes the password for a Windows domain account by using the specified Security Support Provider.
old-location: security\changeaccountpassword.htm
old-project: SecAuthN
ms.assetid: a1d1e315-d1a2-499a-b552-83180508271f
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: ChangeAccountPassword, ChangeAccountPassword function [Security], ChangeAccountPasswordA, ChangeAccountPasswordW, security.changeaccountpassword, sspi/ChangeAccountPassword, sspi/ChangeAccountPasswordA, sspi/ChangeAccountPasswordW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: sspi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ChangeAccountPasswordW (Unicode) and ChangeAccountPasswordA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: SEC_APPLICATION_PROTOCOL_NEGOTIATION_STATUS, *PSEC_APPLICATION_PROTOCOL_NEGOTIATION_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Secur32.dll
api_name:
-	ChangeAccountPassword
-	ChangeAccountPasswordA
-	ChangeAccountPasswordW
product: Windows
targetos: Windows
req.lib: Secur32.lib
req.dll: Secur32.dll
req.irql: 
req.product: Outlook Express 6.0
---

# ChangeAccountPasswordA function


## -description


The <b>ChangeAccountPassword</b> function changes the password for a Windows domain account by using the specified <a href="https://msdn.microsoft.com/91d2389b-1238-49d3-9fef-f1017a8072df">Security Support Provider</a>.

This function is supported only by the <a href="https://msdn.microsoft.com/e7870e72-1386-4818-bf6f-73430ae942a8">Microsoft Kerberos</a>, <a href="https://msdn.microsoft.com/3aa7e979-8b55-416d-bed1-28296055d38e">Microsoft Negotiate</a>, and <a href="https://msdn.microsoft.com/35a38858-d36f-45c9-95f4-2541a182f5ac">Microsoft NTLM</a> providers.


## -parameters




### -param pszPackageName [in]

The name of the provider to use. The value of this parameter must be either "Kerberos", "Negotiate", or "NTLM".


### -param pszDomainName [in]

The domain of the account for which to change the password.


### -param pszAccountName [in]

The user name of the account for which to change the password.


### -param pszOldPassword [in]

The old password to be changed.


### -param pszNewPassword [in]

The new password for the specified account.


### -param bImpersonating [in]

<b>TRUE</b> if the calling process is running as the client; otherwise, <b>FALSE</b>.


### -param dwReserved [in]

Reserved. Must be set to zero.


### -param pOutput [in, out]

On input, a pointer to a <a href="https://msdn.microsoft.com/fc6ef09c-3ba9-4bcb-a3c2-07422af8eaa9">SecBufferDesc</a> structure. The <b>SecBufferDesc</b> structure must contain a single buffer of type <b>SECBUFFER_CHANGE_PASS_RESPONSE</b>. On output, the <b>pvBuffer</b> member of that structure points to a <a href="https://msdn.microsoft.com/7dceaf70-d8de-47c0-b940-f0d6a0cca101">DOMAIN_PASSWORD_INFORMATION</a> structure.


## -returns



If the function succeeds, the function returns SEC_E_OK.

If the function fails, it returns an error code.



