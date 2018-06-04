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

# DsIsMangledRdnValueA function


## -description


The <b>DsIsMangledRdnValue</b> function determines if a given relative distinguished name value is a mangled name of the given type.


## -parameters




### -param pszRdn [in]

Pointer to a null-terminated string that contains  the relative distinguished name  to determine if it is mangled. The <i>cRdn</i> parameter contains the number of characters in this string.


### -param cRdn [in]

Contains the number of characters in the <i>pszRdn</i> string.


### -param eDsMangleForDesired [in]

Contains one of the <a href="https://msdn.microsoft.com/79a66a54-889e-464e-8199-ad911ea84a86">DS_MANGLE_FOR</a> values that specifies the type of name mangling to search for.


## -returns



Returns <b>TRUE</b> if the  relative distinguished name is mangled and the mangle type is the same as specified. Returns <b>FALSE</b> if the relative distinguished name is not mangled or the  mangle type is different than specified.




## -remarks



This function determines if the given relative distinguished name value is mangled and mangled in the given type.  The <i>pszRdn</i> parameter should only contain the value of the relative distinguished name and not the key.  The relative distinguished name value may be quoted or unquoted.




## -see-also




<a href="https://msdn.microsoft.com/79a66a54-889e-464e-8199-ad911ea84a86">DS_MANGLE_FOR</a>



<a href="https://msdn.microsoft.com/a92783c2-ffb8-473e-8484-1c05ca5453ff">Domain Controller and Replication Management Functions</a>



<a href="https://msdn.microsoft.com/e4aaa83c-3bd6-48db-9d34-367b76ba629c">DsIsMangledDn</a>
 

 

