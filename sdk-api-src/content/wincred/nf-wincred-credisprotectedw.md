---
UID: NF:wincred.CredIsProtectedW
title: CredIsProtectedW function
author: windows-sdk-content
description: Specifies whether the specified credentials are encrypted by a previous call to the CredProtect function.
old-location: security\credisprotected.htm
tech.root: secauthn
ms.assetid: 3c38ecf5-1288-4a50-ad17-595e9ff4aaca
ms.author: windowssdkdev
ms.date: 10/01/2018
ms.keywords: CredIsProtected, CredIsProtected function [Security], CredIsProtectedA, CredIsProtectedW, security.credisprotected, wincred/CredIsProtected, wincred/CredIsProtectedA, wincred/CredIsProtectedW
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
req.unicode-ansi: CredIsProtectedW (Unicode) and CredIsProtectedA (ANSI)
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
 - CredIsProtected
 - CredIsProtectedA
 - CredIsProtectedW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CredIsProtectedW function


## -description


 The <b>CredIsProtected</b> function specifies whether the specified credentials are encrypted by a previous call to the <a href="https://msdn.microsoft.com/1e299dfb-2ffe-463c-9e2c-b7774a2216e3">CredProtect</a> function.


## -parameters




### -param pszProtectedCredentials [in]

A pointer to a null-terminated string that specifies the credentials to test.


### -param pProtectionType [out]

A pointer to a value from the <a href="https://msdn.microsoft.com/6d8d8ad6-1b44-4482-a9a2-9c50d522b8d9">CRED_PROTECTION_TYPE</a> enumeration that specifies whether the credentials specified in the <i>pszProtectedCredentials</i> parameter are protected.


## -returns



<b>TRUE</b> if the function succeeds; otherwise, <b>FALSE</b>.

For extended error information, call the 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function.



