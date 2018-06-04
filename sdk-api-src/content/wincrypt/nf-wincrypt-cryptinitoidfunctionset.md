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

# CryptInitOIDFunctionSet function


## -description


The <b>CryptInitOIDFunctionSet</b> initializes and returns the handle of the OID function set identified by a supplied function set name. If the set already exists, the handle of the existing set is returned. If the set does not exist, it is created. This allows different DLLs to install OID functions for the same function set name.


## -parameters




### -param pszFuncName [in]

Name of the OID function set.


### -param dwFlags [in]

Reserved for future use and must be zero.


## -returns



Returns the handle of the OID function set identified by <i>pszFuncName</i>, or <b>NULL</b> if the function fails.




## -see-also




<a href="cryptography_functions.htm">OID Support Functions</a>
 

 

