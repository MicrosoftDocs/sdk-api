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

# OLECMDEXECOPT enumeration


## -description


Specifies command execution options.


## -enum-fields




### -field OLECMDEXECOPT_DODEFAULT

Prompt the user for input or not, whichever is the default behavior.


### -field OLECMDEXECOPT_PROMPTUSER

Execute the command after obtaining user input.


### -field OLECMDEXECOPT_DONTPROMPTUSER

Execute the command without prompting the user. For example, clicking the Print toolbar button causes a document to be immediately printed without user input.


### -field OLECMDEXECOPT_SHOWHELP

Show help for the corresponding command, but do not execute.



## -see-also




<a href="https://msdn.microsoft.com/a2071ca9-8675-4f53-b30e-8c7198c2acca">IOleCommandTarget::Exec</a>
 

 

