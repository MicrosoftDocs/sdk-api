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

# _SECPKG_SUPPLEMENTAL_CRED_ARRAY structure


## -description


The <b>SECPKG_SUPPLEMENTAL_CRED_ARRAY</b> structure contains <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">supplemental credentials</a> information. This structure is used by the 
<a href="https://msdn.microsoft.com/002ac773-bd46-49b5-b54c-6b8f5d5ef9f7">LsaApLogonUserEx2</a> and 
<a href="https://msdn.microsoft.com/952ed682-775a-4370-8a89-15ca35553667">UpdateCredentials</a> functions.


## -struct-fields




### -field CredentialCount

The number of supplemental credentials in the <b>Credentials</b> member.


### -field Credentials.size_is

 


### -field Credentials.size_is.CredentialCount

 


### -field Credentials

An array containing supplemental credentials.

