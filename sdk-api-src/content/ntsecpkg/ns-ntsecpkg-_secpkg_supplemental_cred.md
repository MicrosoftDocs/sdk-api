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

# _SECPKG_SUPPLEMENTAL_CRED structure


## -description


The <b>SECPKG_SUPPLEMENTAL_CRED</b> structure contains <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">supplemental credentials</a> recognized by the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security package</a>.

The structure is used by the 
<a href="https://msdn.microsoft.com/bb382937-e5d6-452b-b166-505d0c80412c">SpAcceptCredentials</a> function and the 
<a href="https://msdn.microsoft.com/b9514e26-29a5-4ba8-a375-1723c0a1ce39">SECPKG_SUPPLEMENTAL_CRED_ARRAY</a> structure.


## -struct-fields




### -field PackageName

The name of the <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">authentication package</a> that authenticated the <a href="https://msdn.microsoft.com/library/windows/hardware/dn922689">credentials</a>.


### -field CredentialSize

The size of the <b>Credentials</b> member, in bytes.


### -field Credentials

Pointer to a set of package-specific supplemental credentials.


### -field Credentials.size_is

 


### -field Credentials.size_is.CredentialSize

 



