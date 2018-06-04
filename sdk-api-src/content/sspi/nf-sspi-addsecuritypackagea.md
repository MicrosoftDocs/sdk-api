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

# AddSecurityPackageA function


## -description


Adds a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security support provider</a> to the list of providers supported by <a href="https://msdn.microsoft.com/3aa7e979-8b55-416d-bed1-28296055d38e">Microsoft Negotiate</a>.


## -parameters




### -param pszPackageName [in]

The name of the package to add.


### -param pOptions [in]

A pointer to a <a href="https://msdn.microsoft.com/2e9f65ec-72a5-4d6f-aa63-f83369f0dd07">SECURITY_PACKAGE_OPTIONS</a> structure that specifies additional information about the security package.


## -returns




						If the function succeeds, it returns <b>SEC_E_OK</b>.

If the function fails, it returns a nonzero error code.




## -see-also




<a href="https://msdn.microsoft.com/7a9a2c64-92a4-419b-8b20-d0f5cba64147">DeleteSecurityPackage</a>
 

 

