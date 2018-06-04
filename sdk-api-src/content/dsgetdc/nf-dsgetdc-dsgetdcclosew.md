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

# DsGetDcCloseW function


## -description


The <b>DsGetDcClose</b>  function closes a domain controller enumeration operation.


## -parameters




### -param GetDcContextHandle [in]

Contains the domain controller enumeration context handle provided by the <a href="https://msdn.microsoft.com/2811cc30-f367-4f1a-8f0c-ed0a77dad24c">DsGetDcOpen</a> function.


## -returns



This function does not return a value.




## -remarks



When this function is called, <i>GetDcContextHandle</i> is invalid and cannot be used.




## -see-also




<a href="https://msdn.microsoft.com/7b519c81-5a6c-470a-a525-1894efd53305">Directory Service Functions</a>



<a href="https://msdn.microsoft.com/2811cc30-f367-4f1a-8f0c-ed0a77dad24c">DsGetDcOpen</a>



<a href="https://msdn.microsoft.com/bfc92777-6944-406a-8b93-949a1cf3e2c3">Enumerating Domain Controllers</a>
 

 

