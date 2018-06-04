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

# D2D1_LINE_JOIN enumeration


## -description


Describes the shape that joins two lines or segments. 




## -enum-fields




### -field D2D1_LINE_JOIN_MITER

Regular angular vertices. 


### -field D2D1_LINE_JOIN_BEVEL

Beveled vertices.   


### -field D2D1_LINE_JOIN_ROUND

Rounded vertices. 


### -field D2D1_LINE_JOIN_MITER_OR_BEVEL

Regular angular vertices unless the join would extend beyond the miter limit; otherwise, beveled vertices.  


### -field D2D1_LINE_JOIN_FORCE_DWORD




## -remarks




          A miter limit affects how sharp miter joins are allowed to be.
	If the line join style is <b>D2D1_LINE_JOIN_MITER_OR_BEVEL</b>, then the join will be mitered with regular angular vertices if it doesn't extend
	beyond the miter limit; otherwise, the line join will be beveled.

The following illustration shows  different line join settings for the same stroked path geometry.  

<img alt="Illustration of line join settings" src="images/StrokeStyle_Join.png"/>



