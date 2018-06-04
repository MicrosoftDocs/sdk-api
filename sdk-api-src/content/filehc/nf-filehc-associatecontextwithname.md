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

# AssociateContextWithName function


## -description


Inserts a name into the name cache to find a specified <a href="Http://go.microsoft.com/fwlink/p/?linkid=85304">FIO_CONTEXT</a> structure.


## -parameters




### -param pNameCache [in]

A pointer to the name of the cache to be used.


### -param lpbName [in]

User-specified bytes for the name of the cache item.


### -param cbName [in]

The length of the name that is assigned to the cache item.


### -param lpbData [in]

User-specified bytes for any arbitrary data to associate with the name of the cache item.


### -param cbData [in]

The length, in bytes, of arbitrary data to associate with the name.


### -param pGenericMapping [in]

A pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff546526">GENERIC_MAPPING</a> structure to associate with the name.


### -param pSecurityDescriptor [in]

The self-relative security descriptor to be associated with the name. This descriptor is provided by the user.


### -param pContext [in]

A pointer to an <a href="Http://go.microsoft.com/fwlink/p/?linkid=85304">FIO_CONTEXT</a> structure.


### -param fKeepReference [in]

Specifies whether the reference on the <a href="Http://go.microsoft.com/fwlink/p/?linkid=85304">FIO_CONTEXT</a> structure should be kept. If set to <b>TRUE</b>, the reference is kept.


## -returns



Returns <b>TRUE</b> if the function succeeds; otherwise, it returns <b>FALSE</b>.




## -remarks



If the name is already present in the cache, this call fails and <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> returns ERROR_DUP_NAME.




## -see-also




<a href="Http://go.microsoft.com/fwlink/p/?linkid=85304">FIO_CONTEXT</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff546526">GENERIC_MAPPING</a>
 

 

