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

# ChangeAccountPasswordW function


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



