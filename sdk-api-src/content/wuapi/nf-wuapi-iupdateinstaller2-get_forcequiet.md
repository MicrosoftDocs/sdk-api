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

# IUpdateInstaller2::get_ForceQuiet


## -description


Gets and sets a Boolean value that indicates whether Windows Installer is forced to install the updates without user interaction.

This property is read/write.


## -parameters


## -remarks



You cannot forcibly silence some updates. If an update does not support this action, and you try to install the update, the update returns the following: WU_E_UH_DOESNOTSUPPORTACTION.




## -see-also




<a href="https://msdn.microsoft.com/89edc91d-59a1-4e23-9adb-fc3027e2e898">IUpdateInstaller2</a>
 

 

