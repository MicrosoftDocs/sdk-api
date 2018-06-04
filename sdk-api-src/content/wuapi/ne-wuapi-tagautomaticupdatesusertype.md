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

# tagAutomaticUpdatesUserType enumeration


## -description


Defines the type of user.


## -enum-fields




### -field auutCurrentUser

The context of the current user.


### -field auutLocalAdministrator

Any administrator on the local computer.


## -remarks



The AutomaticUpdatesUserType is used in conjunction with the <a href="https://msdn.microsoft.com/fbf36d9f-98c1-4b9d-b479-a9203b6ce952">IAutomaticUpdatesSettings2::CheckPermission</a> method.



