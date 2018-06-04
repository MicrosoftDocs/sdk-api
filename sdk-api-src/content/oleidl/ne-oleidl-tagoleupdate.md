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

# tagOLEUPDATE enumeration


## -description


Indicates whether the linked object updates the cached data for the linked object automatically or only when the container calls either the <a href="https://msdn.microsoft.com/1743f99b-4c3b-47be-b77b-1d3378a44903">IOleObject::Update</a> or <a href="https://msdn.microsoft.com/c1da8b95-88e7-42b0-884c-5aa394cc49f4">IOleLink::Update</a> methods. The constants are used in the <a href="https://msdn.microsoft.com/4a34a90d-df1b-4bbf-8365-9d741c18ff74">IOleLink</a> interface. 




## -enum-fields




### -field OLEUPDATE_ALWAYS

Update the link object whenever possible, this option corresponds to the <b>Automatic update</b> option in the <b>Links</b> dialog box.


### -field OLEUPDATE_ONCALL

Update the link object only when <a href="https://msdn.microsoft.com/1743f99b-4c3b-47be-b77b-1d3378a44903">IOleObject::Update</a> or <a href="https://msdn.microsoft.com/c1da8b95-88e7-42b0-884c-5aa394cc49f4">IOleLink::Update</a> is called, this option corresponds to the <b>Manual update</b> option in the <b>Links</b> dialog box.



## -see-also




<a href="https://msdn.microsoft.com/2cb91b48-0026-4afa-80ab-16ac6fbce04d">IOleLink::GetUpdateOptions</a>



<a href="https://msdn.microsoft.com/310c25b5-a2f6-4ed7-8673-c53809fad32f">IOleLink::SetUpdateOptions</a>
 

 

