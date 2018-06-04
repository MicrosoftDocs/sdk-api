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

# DSA_NEWOBJ_DISPINFO structure


## -description


The <b>DSA_NEWOBJ_DISPINFO</b> structure is used with the <a href="https://msdn.microsoft.com/38dd4f43-6f8f-460a-9c5d-0a506d993101">IDsAdminNewObjExt::Initialize</a> method to supply additional data about an Active Directory Domain Services  object creation wizard.


## -struct-fields




### -field dwSize

Contains the size, in bytes, of the structure. This member is used for versioning purposes.


### -field hObjClassIcon

Contains the handle  of the class icon for the object created.


### -field lpszWizTitle

Pointer to a null-terminated Unicode string that contains the title of the wizard.


### -field lpszContDisplayName

Pointer to a null-terminated Unicode string that contains the display name, or canonical name,  of the container the object is created in.


## -see-also




<a href="https://msdn.microsoft.com/38dd4f43-6f8f-460a-9c5d-0a506d993101">IDsAdminNewObjExt::Initialize</a>
 

 

