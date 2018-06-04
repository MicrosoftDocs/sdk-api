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

# tagUSERCLASSTYPE enumeration


## -description


Indicates the different variants of the display name associated with a class of objects.


## -enum-fields




### -field USERCLASSTYPE_FULL

The full type name of the class.


### -field USERCLASSTYPE_SHORT

A short name (maximum of 15 characters) that is used for popup menus and the <b>Links</b> dialog box.


### -field USERCLASSTYPE_APPNAME

The name of the application servicing the class and is used in the result text in dialog boxes.


## -see-also




<a href="https://msdn.microsoft.com/8ffffa01-d118-4955-84d1-a4659ba9ddc9">IOleObject::GetUserType</a>



<a href="https://msdn.microsoft.com/492a4084-494e-4d78-8f3a-853ec486a2d6">OleRegGetUserType</a>
 

 

