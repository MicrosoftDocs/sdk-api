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

# SspiPrepareForCredWrite function


## -description


Generates values from an identity structure that can be passed as the values of parameters in a call to the <a href="https://msdn.microsoft.com/9a590347-d610-4916-bf63-60fbec173ac2">CredWrite</a> function.


## -parameters




### -param AuthIdentity [in]

The identity structure from which to generate the credentials to be passed to the <a href="https://msdn.microsoft.com/9a590347-d610-4916-bf63-60fbec173ac2">CredWrite</a> function.


### -param pszTargetName [in]

A target name that can be modified by this function depending on the value of the <i>AuthIdentity</i> parameter.

Set the value of this parameter to <b>NULL</b> to use the user name as the target.


### -param pCredmanCredentialType [out]

The credential type to pass to the <a href="https://msdn.microsoft.com/9a590347-d610-4916-bf63-60fbec173ac2">CredWrite</a> function.


### -param ppszCredmanTargetName [out]

The target name to pass to the <a href="https://msdn.microsoft.com/9a590347-d610-4916-bf63-60fbec173ac2">CredWrite</a> function.


### -param ppszCredmanUserName [out]

The user name to pass to the <a href="https://msdn.microsoft.com/9a590347-d610-4916-bf63-60fbec173ac2">CredWrite</a> function.


### -param ppCredentialBlob [out]

The credential <a href="https://msdn.microsoft.com/2e570727-7da0-4e17-bf5d-6fe0e6aef65b">BLOB</a> to send to the <a href="https://msdn.microsoft.com/9a590347-d610-4916-bf63-60fbec173ac2">CredWrite</a> function.


### -param pCredentialBlobSize [out]

The size, in bytes, of the <i>ppCredentialBlob</i> buffer.


## -returns




						If the function succeeds, it returns <b>SEC_E_OK</b>.

If the function fails, it returns a nonzero error code.



