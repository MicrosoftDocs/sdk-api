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

# _tagOLECMDTEXT structure


## -description


Specifies a text name or status string for a single command identifier.


## -struct-fields




### -field cmdtextf

A value from the <a href="https://msdn.microsoft.com/8978331a-33b6-4f57-b5a3-aae305c1d872">OLECMDTEXTF</a> enumeration describing whether the <b>rgwz</b> member contains a command name or status text.


### -field cwActual

The number of characters actually written into the <b>rgwz</b> buffer before <a href="https://msdn.microsoft.com/8acbf788-f113-43d9-800d-aad84db24498">IOleCommandTarget::QueryStatus</a> returns.


### -field cwBuf

The number of elements in the <b>rgwz</b> array.


### -field rgwz

A caller-allocated array of wide characters to receive the command name or status text.



## -see-also




<a href="https://msdn.microsoft.com/8acbf788-f113-43d9-800d-aad84db24498">IOleCommandTarget::QueryStatus</a>



<a href="https://msdn.microsoft.com/8978331a-33b6-4f57-b5a3-aae305c1d872">OLECMDTEXTF</a>
 

 

