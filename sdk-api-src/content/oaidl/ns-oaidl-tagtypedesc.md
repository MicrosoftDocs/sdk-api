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

# tagTYPEDESC structure


## -description


Describes the type of a variable, the return type of a function, or the type of a function parameter.


## -struct-fields




### -field DUMMYUNIONNAME

 


### -field DUMMYUNIONNAME.lptdesc

 With VT_PTR, the type pointed to.


### -field DUMMYUNIONNAME.lpadesc

With VT_CARRAY...


### -field DUMMYUNIONNAME.hreftype

With VT_USER_DEFINED, this is used to get a TypeInfo for the UDT.


### -field vt

The variant type.


## -remarks



If the variable is VT_SAFEARRAY or VT_PTR, the union portion of the TYPEDESC contains a pointer to a TYPEDESC that specifies the element type.



