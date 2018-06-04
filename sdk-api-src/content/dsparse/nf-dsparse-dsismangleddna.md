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

# DsIsMangledDnA function


## -description


The <b>DsIsMangledDn</b> function determines if the first relative distinguished name (RDN) in a distinguished name (DN) is a mangled name of a given type.


## -parameters




### -param pszDn [in]

Pointer to a null-terminated string that contains the  distinguished name to retrieve the relative distinguished name from. This can also be a quoted distinguished name  as returned by other directory service functions.


### -param eDsMangleFor [in]

Contains one of the <a href="https://msdn.microsoft.com/79a66a54-889e-464e-8199-ad911ea84a86">DS_MANGLE_FOR</a> values that specifies the type of name mangling to look for.


## -returns



Returns <b>TRUE</b> if the first relative distinguished name in <i>pszDn</i> is mangled in the manner specified by <i>eDsMangleFor</i> or <b>FALSE</b>  otherwise.




## -see-also




<a href="https://msdn.microsoft.com/79a66a54-889e-464e-8199-ad911ea84a86">DS_MANGLE_FOR</a>



<a href="https://msdn.microsoft.com/a92783c2-ffb8-473e-8484-1c05ca5453ff">Domain Controller and Replication Management Functions</a>



<a href="https://msdn.microsoft.com/adf5e133-9e48-4e97-af0c-4f8ea9b8bf8f">DsIsMangledRdnValue</a>
 

 

