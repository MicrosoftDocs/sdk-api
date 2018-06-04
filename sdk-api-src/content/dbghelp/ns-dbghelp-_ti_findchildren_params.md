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

# _TI_FINDCHILDREN_PARAMS structure


## -description


Contains type index information. It is used by the 
<a href="https://msdn.microsoft.com/bc94a5b1-d49d-425a-89a8-c584c3979930">SymGetTypeInfo</a> function.


## -struct-fields




### -field Count

The number of children.


### -field Start

The zero-based index of the child from which the child indexes are to be retrieved. For example, in an array with five elements, if Start is two, this indicates the third array element. In most cases, this member is zero.


### -field ChildId

An array of type indexes. There is one index per child.


## -see-also




<a href="https://msdn.microsoft.com/bc94a5b1-d49d-425a-89a8-c584c3979930">SymGetTypeInfo</a>
 

 

