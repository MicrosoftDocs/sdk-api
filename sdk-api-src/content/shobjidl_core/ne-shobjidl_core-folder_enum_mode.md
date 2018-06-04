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

# FOLDER_ENUM_MODE enumeration


## -description


Used by <a href="https://msdn.microsoft.com/5d331255-2295-4f7b-b2d6-1238edcc15bb">IObjectWithFolderEnumMode::GetMode</a> and <a href="https://msdn.microsoft.com/7e7271ec-47a7-42bf-ab02-26cd587448bd">IObjectWithFolderEnumMode::SetMode</a> methods to get and set the display modes for the folders.


## -enum-fields




### -field FEM_VIEWRESULT

 Display mode to view the contents of a folder.


### -field FEM_NAVIGATION

 Display mode to view the contents of the folders in the navigation pane.


## -remarks



If an item does not support the enumeration mode value (because it is not a folder or it does not provide the enumeration mode) then it is created in the default enumeration mode.



