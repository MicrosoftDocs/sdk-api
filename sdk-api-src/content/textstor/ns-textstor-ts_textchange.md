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

# TS_TEXTCHANGE structure


## -description



The <b>TS_TEXTCHANGE</b> structure contains text change data.




## -struct-fields




### -field acpStart

Contains the starting character position of the change.


### -field acpOldEnd

Contains the ending character position before the text is changed.


### -field acpNewEnd

Contains the ending character position after the text is changed.


## -remarks



The possible text changes include insert, delete, and replace. For example, if you replace the first "t" of "text" with "T", <b>acpStart</b> =0, <b>acpOldEnd</b> =1, and <b>acpNewEnd</b> =1. If you delete the last "t", <b>acpStart</b> =3, <b>acpOldEnd</b> =4, and <b>acpNewEnd</b> =3. If an "a" is inserted between "e" and "x", <b>acpStart</b> =2, <b>acpOldEnd</b> =2, and <b>acpNewEnd</b> =3.



