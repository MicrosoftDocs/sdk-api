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

# CredFindBestCredentialA function


## -description


The <b>CredFindBestCredential</b> function searches the <a href="https://msdn.microsoft.com/0c44a360-d9c3-448c-a0d5-e33f3c27c58c">Credentials Management</a> (CredMan) database for the set of generic credentials that are associated with the current logon session and that best match the specified target resource.


## -parameters




### -param TargetName [in]

A pointer to a null-terminated string that contains the name of the target resource for which to find credentials.


### -param Type [in]

The type of credentials to search for. Currently, this function supports only <b>CRED_TYPE_GENERIC</b>.


### -param Flags [in]

Reserved.


### -param Credential [out]

The address of a pointer to a <a href="https://msdn.microsoft.com/6361b93c-4441-4a01-bd39-b95c42962497">CREDENTIAL</a> structure that specifies the set of credentials this function finds.

When you have finished using this structure, free it by calling the <a href="https://msdn.microsoft.com/bc33ab1b-dd3f-4e1b-96d2-e32ceff89ada">CredFree</a> function.


## -returns




						If the function succeeds, it returns <b>TRUE</b>.

If the function fails, it returns <b>FALSE</b>. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.



