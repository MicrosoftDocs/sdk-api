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

# urlassociationdialog_in_flags enumeration


## -description


The <b>URLASSOCIATIONDIALOG_IN_FLAGS</b> enumerated values are used with <a href="https://msdn.microsoft.com/3158e819-f131-4f57-8516-998955100377">URLAssociationDialog</a> to determine how it executes.


## -enum-fields




### -field URLASSOCDLG_FL_USE_DEFAULT_NAME

Use the default file name (that is, "Internet Shortcut").


### -field URLASSOCDLG_FL_REGISTER_ASSOC

Register the selected application as the handler for the protocol specified in the <i>pcszURL</i> parameter of <a href="https://msdn.microsoft.com/3158e819-f131-4f57-8516-998955100377">URLAssociationDialog</a>. The application is registered only if this flag is set and the user indicates that a persistent association is desired.

