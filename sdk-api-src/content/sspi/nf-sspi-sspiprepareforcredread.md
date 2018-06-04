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

# SspiPrepareForCredRead function


## -description


Generates a target name and credential type from the specified identity structure.

The values that this function generates can be passed as the values of the <i>TargetName</i> and <i>Type</i> parameters in a call to the <a href="https://msdn.microsoft.com/3222de7b-5290-4e82-a382-b2db6afc78cc">CredRead</a> function.


## -parameters




### -param AuthIdentity [in]

The identity structure from which to generate the credentials to be passed to the <a href="https://msdn.microsoft.com/3222de7b-5290-4e82-a382-b2db6afc78cc">CredRead</a> function.


### -param pszTargetName [in]

A target name that can be modified by this function depending on the value of the <i>AuthIdentity</i> parameter.


### -param pCredmanCredentialType [out]

The credential type to pass to the <a href="https://msdn.microsoft.com/3222de7b-5290-4e82-a382-b2db6afc78cc">CredRead</a> function.


### -param ppszCredmanTargetName [out]

The target name to pass to the <a href="https://msdn.microsoft.com/3222de7b-5290-4e82-a382-b2db6afc78cc">CredRead</a> function.


## -returns




						If the function succeeds, it returns <b>SEC_E_OK</b>.

If the function fails, it returns a nonzero error code.



