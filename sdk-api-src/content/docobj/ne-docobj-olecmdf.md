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

# OLECMDF enumeration


## -description


Specifies the type of support provided by an object for the command specified in an <a href="https://msdn.microsoft.com/a75ca136-ed6a-43c5-b775-a50535431f1d">OLECMD</a> structure.


## -enum-fields




### -field OLECMDF_SUPPORTED

The command is supported by this object.


### -field OLECMDF_ENABLED

The command is available and enabled.


### -field OLECMDF_LATCHED

The command is an on-off toggle and is currently on.


### -field OLECMDF_NINCHED

Reserved for future use.



### -field OLECMDF_INVISIBLE

The command is hidden.


### -field OLECMDF_DEFHIDEONCTXTMENU

The command is hidden on the context menu.


## -remarks



Values from the <b>OLECMDF</b> enumeration are used to fill the value of the <b>cmdf</b> member of <a href="https://msdn.microsoft.com/a75ca136-ed6a-43c5-b775-a50535431f1d">OLECMD</a> structures passed to <a href="https://msdn.microsoft.com/8acbf788-f113-43d9-800d-aad84db24498">IOleCommandTarget::QueryStatus</a>.




## -see-also




<a href="https://msdn.microsoft.com/8acbf788-f113-43d9-800d-aad84db24498">IOleCommandTarget::QueryStatus</a>



<a href="https://msdn.microsoft.com/a75ca136-ed6a-43c5-b775-a50535431f1d">OLECMD</a>
 

 

