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

# _tagAUTOCOMPLETELISTOPTIONS enumeration


## -description


Specifies which objects are enumerated for autocompletion lists.


## -enum-fields




### -field ACLO_NONE

No enumeration should take place.


### -field ACLO_CURRENTDIR

Only the current directory should be enumerated.


### -field ACLO_MYCOMPUTER

Only MyComputer should be enumerated.


### -field ACLO_DESKTOP

Only the Desktop Folder should be enumerated.


### -field ACLO_FAVORITES

Only the Favorites Folder should be enumerated.


### -field ACLO_FILESYSONLY

Only the file system should be enumerated.


### -field ACLO_FILESYSDIRS

<b>Internet Explorer 6 or greater:</b> The file system dirs, UNC shares, and UNC servers should be enumerated.


### -field ACLO_VIRTUALNAMESPACE

<b>Windows Internet Explorer 7 or greater:</b> The virtual namespace should be enumerated.

