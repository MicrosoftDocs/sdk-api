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

# FILE_USAGE_TYPE enumeration


## -description


Constants used by <a href="https://msdn.microsoft.com/7baba34d-b246-4d48-9f0c-e950d33ed5cf">IFileIsInUse::GetUsage</a> to indicate how a file in use is being used.


## -enum-fields




### -field FUT_PLAYING

The file is being played by the process that has it open.


### -field FUT_EDITING

The file is being edited by the process that has it open.


### -field FUT_GENERIC

The file is open in the process for an unspecified action or an action that does not readily fit into the other two categories.


## -remarks



The interpretation of "playing" or "editing" is left to the application's implementation of <a href="https://msdn.microsoft.com/68a4ab3d-165e-4917-8915-77f15901dbad">IFileIsInUse</a>. Generally, "playing" would refer to a media file while "editing" can refer to any file being altered in an application. However, the application itself best knows how to map these terms to its actions.



