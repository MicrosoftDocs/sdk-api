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

# __MIDL___MIDL_itf_pla_0001_0043_0012 enumeration


## -description


Defines the action that the data manager takes when both the age and size limits are met.


## -enum-fields




### -field plaCreateCab

Creates a cabinet file. The name of the cabinet file is  <i>nameofthesubfolder</i>.cab.


### -field plaDeleteData

Deletes all files in the folder, except the report and cabinet file.


### -field plaSendCab

Sends the cabinet file to the location specified in the <a href="https://msdn.microsoft.com/a6398d07-f15d-401b-a3b6-21b2506ad270">IFolderAction::SendCabTo</a> property.


### -field plaDeleteCab

Deletes the cabinet file.


### -field plaDeleteReport

Deletes the report file.


## -remarks



Specify one or more actions. The data manager applies the actions in the order in which they are defined in this enumeration.




## -see-also




<a href="https://msdn.microsoft.com/7e7672d9-9384-4365-aa4a-bf8dace050c2">IFolderAction::Actions</a>
 

 

