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

# ObjectTypeIsValid function


## -description


The <b>ObjectTypeIsValid</b> function determines whether an element of the ObjectType enumeration represents a valid object type.


## -parameters




### -param type

Type: <b><a href="https://msdn.microsoft.com/9b35cac6-62e7-4ca2-98e2-2a983da565c1">ObjectType</a></b>

Element of the ObjectType enumeration to be tested.


## -returns



Type: <strong>Type: <b>BOOL</b>
</strong>

If objectType is equal to ObjectTypeInvalid, this function returns <b>FALSE</b>.

 If objectType is equal to any other element of the ObjectType enumeration, this function returns <b>TRUE</b>.



