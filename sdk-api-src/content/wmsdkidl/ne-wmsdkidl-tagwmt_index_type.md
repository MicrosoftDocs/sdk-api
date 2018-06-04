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

# tagWMT_INDEX_TYPE enumeration


## -description



The <b>WMT_INDEX_TYPE</b> enumeration type defines the type of object that will be associated with an index. Because the time specified by an index will not usually correspond exactly with an object in the file, the indexer must associate the index with an object in the bit stream close to the specified time.




## -enum-fields




### -field WMT_IT_NEAREST_DATA_UNIT

The index will associate indexes with the nearest data unit, or packet, in the Windows Media file.


### -field WMT_IT_NEAREST_OBJECT

The index will associate indexes with the nearest data object, or compressed sample, in the Windows Media file.


### -field WMT_IT_NEAREST_CLEAN_POINT

The index will associate indexes with the nearest <a href="wmformat_glossary.htm">cleanpoint</a>, or video key frame, in the Windows Media file. This is the default index type.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff545452">Enumeration Types</a>
 

 

