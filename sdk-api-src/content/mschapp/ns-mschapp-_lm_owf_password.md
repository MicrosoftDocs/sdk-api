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

# _LM_OWF_PASSWORD structure


## -description


The <b>LM_OWF_PASSWORD</b> stores the Lan Manage (LM) one-way function (OWF) of a user's password.


## -struct-fields




### -field data

An array of <a href="https://msdn.microsoft.com/eb0e38ed-8d12-4df2-be58-7ac18447121f">CYPHER_BLOCK</a> structures that contain a LM OWF password hash. The contents of the array are calculated using the <b>LmEncryptedPasswordHash()</b> function as defined in <a href="http://go.microsoft.com/fwlink/p/?linkid=84041">RFC 2433</a>, section A.8.


## -remarks




<a href="https://msdn.microsoft.com/7edba7de-e3b8-4a93-b70b-19c68541da1e">NT_OWF_PASSWORD</a> is an alias for this structure.




## -see-also




<a href="https://msdn.microsoft.com/adee58bd-d2aa-4570-8c43-50240be02ed3">MS-CHAP Password Management Structures</a>



<a href="https://msdn.microsoft.com/6c154675-4c82-4305-8231-577f990eaeb1">MSChapSrvChangePassword</a>
 

 

