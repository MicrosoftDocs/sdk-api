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

# FAX_COVERPAGE_TYPE_ENUM enumeration


## -description


The <b>FAX_COVERPAGE_TYPE_ENUM</b> enumeration defines whether a cover page template file is a local computer cover page or a server-based cover page. It can also specify that no file is used. 


## -enum-fields




### -field fcptNONE

No cover page.


### -field fcptLOCAL

Use a cover page from local computer.


### -field fcptSERVER

Use a cover page from the fax server common coverpages folder. 


## -see-also




<a href="https://msdn.microsoft.com/ca6b43c6-7b06-448c-b715-3c92a5c4a853">IFaxDocument::get_CoverPageType</a>
 

 

