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

# Metafile class


## -description


The <b>Metafile</b> class defines a graphic metafile. A metafile contains records that describe a sequence of graphics API calls. Metafiles can be recorded (constructed) and played back (displayed).


## -remarks



Some <a href="https://msdn.microsoft.com/a9648287-65d9-47d8-b32b-33f74b4fcd07">Metafile</a> constructors (those that receive a device context handle) create <b>Metafile</b> objects that are used to record metafiles. Other Metafile constructors (those that do not receive a device context handle) create <b>Metafile</b> objects that are used to display (play back) metafiles. 



