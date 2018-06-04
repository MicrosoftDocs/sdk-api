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

# CredIsProtectedA function


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



