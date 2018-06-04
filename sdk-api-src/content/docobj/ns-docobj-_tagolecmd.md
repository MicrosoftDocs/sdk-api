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

# _tagOLECMD structure


## -description


Associates command flags from the <a href="https://msdn.microsoft.com/feb493da-0db2-4251-ba6f-ded1fbd3e430">OLECMDF</a> enumeration with a command identifier through a call to <a href="https://msdn.microsoft.com/8acbf788-f113-43d9-800d-aad84db24498">IOleCommandTarget::QueryStatus</a>.




## -struct-fields




### -field cmdID

A command identifier; taken from the <a href="https://msdn.microsoft.com/ae1592b6-2afd-4379-a18e-d46b226bc9e2">OLECMDID</a> enumeration.


### -field cmdf

Flags associated with <b>cmdID</b>; taken from the <a href="https://msdn.microsoft.com/feb493da-0db2-4251-ba6f-ded1fbd3e430">OLECMDF</a> enumeration.



## -see-also




<a href="https://msdn.microsoft.com/8acbf788-f113-43d9-800d-aad84db24498">IOleCommandTarget::QueryStatus</a>



<a href="https://msdn.microsoft.com/feb493da-0db2-4251-ba6f-ded1fbd3e430">OLECMDF</a>
 

 

