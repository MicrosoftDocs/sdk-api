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

# EXPLORER_BROWSER_FILL_FLAGS enumeration


## -description


These flags are used with <a href="https://msdn.microsoft.com/f978d5d1-a597-4e49-9a2a-de23e99bf65e">IExplorerBrowser::FillFromObject</a>.


## -enum-fields




### -field EBF_NONE

No flags.


### -field EBF_SELECTFROMDATAOBJECT

Causes <a href="https://msdn.microsoft.com/f978d5d1-a597-4e49-9a2a-de23e99bf65e">IExplorerBrowser::FillFromObject</a> to first populate the results folder with the contents of the parent folders of the items in the data object, and then select only the items that are in the data object.


### -field EBF_NODROPTARGET

Do not allow dropping on the folder. In other words, do not register a drop target for the view. Applications can then register their own drop targets.

