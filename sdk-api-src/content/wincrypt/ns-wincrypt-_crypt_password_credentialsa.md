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

# _CRYPT_PASSWORD_CREDENTIALSA structure


## -description


The <b>CRYPT_PASSWORD_CREDENTIALS</b> structure contains the user name and password credentials to be used in the <a href="https://msdn.microsoft.com/d28b2f52-3258-44ad-a3ab-0743d3afcd62">CRYPT_CREDENTIALS</a> structure as optional input to a remote object retrieval function such as <a href="https://msdn.microsoft.com/2e205f97-be9b-4358-ba22-d475b6a250b7">CryptRetrieveObjectByUrl</a> or <a href="https://msdn.microsoft.com/dd639b43-1560-4e9f-a778-9e20484ae012">CryptGetTimeValidObject</a>.


## -struct-fields




### -field cbSize

The size, in bytes, of this structure.


### -field pszUsername

A pointer to a null-terminated string that contains the user name credential for the remote session authentication.


### -field pszPassword

A pointer to a null-terminated string that contains the password credential for the remote session authentication.

