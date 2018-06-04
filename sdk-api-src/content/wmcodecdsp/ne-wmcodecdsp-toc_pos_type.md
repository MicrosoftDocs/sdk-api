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

# TOC_POS_TYPE enumeration


## -description


The <b>TOC_POS_TYPE</b> enumeration contains members that specify the <a href="https://msdn.microsoft.com/cc2fbadc-43f7-470c-873b-de2dc9d84e5d">position type</a> of a table of contents.


## -enum-fields




### -field TOC_POS_INHEADER

Specifies that the table of contents is stored in the header of the media file.


### -field TOC_POS_TOPLEVELOBJECT

Specifies that the table of contents is stored in the body of the media file as a top level object.


## -remarks



Currently, only <b>TOC_POS_TOPLEVELOBJECT</b> is supported.




## -see-also




<a href="https://msdn.microsoft.com/d414c0d7-e3f1-4697-8ab1-f38815eaf889">Table of Contents Parser Enumerations</a>



<a href="https://msdn.microsoft.com/cc2fbadc-43f7-470c-873b-de2dc9d84e5d">The Position Type of a Table of Contents</a>
 

 

