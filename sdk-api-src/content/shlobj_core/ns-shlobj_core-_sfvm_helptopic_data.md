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

# _SFVM_HELPTOPIC_DATA structure


## -description


Contains the name of an HTML Help file and a topic in that file. Used with the <a href="https://msdn.microsoft.com/bbe92e9f-4074-4101-a945-072866ab20a8">SFVM_GETHELPTOPIC</a> notification. This structure requires Unicode strings.


## -struct-fields




### -field wszHelpFile

Type: <b>WCHAR[MAX_PATH]</b>

A null-terminated Unicode string containing the fully qualified path to the help file.


### -field wszHelpTopic

Type: <b>WCHAR[MAX_PATH]</b>

A null-terminated Unicode string containing the name of the topic.

