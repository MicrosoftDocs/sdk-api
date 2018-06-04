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

# mimeassociationdialog_in_flags enumeration


## -description


Used with the <a href="https://msdn.microsoft.com/0f8ee95a-3f95-47ee-822b-740ba134cd3c">MIMEAssociationDialog</a> function to determine how it executes.


## -enum-fields




### -field MIMEASSOCDLG_FL_REGISTER_ASSOC

If this bit is set, the selected application is registered as the handler for the given MIME type. If this bit is clear, no association is registered.


## -remarks



An application is registered only if this flag is set and the user indicates that a persistent association is to be made.



