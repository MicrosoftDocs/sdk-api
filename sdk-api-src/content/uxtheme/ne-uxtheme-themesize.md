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

# THEMESIZE enumeration


## -description


Identifies the type of size value to retrieve for a visual style part.


## -enum-fields




### -field TS_MIN

Receives the minimum size of a visual style part.


### -field TS_TRUE

Receives the size of the visual style part that will best fit the available space.


### -field TS_DRAW

Receives the size that the theme manager uses to draw a part.


## -remarks



A value from the <b>THEMESIZE</b> enumeration is used with the <a href="https://msdn.microsoft.com/0da9bbbc-ff63-45a7-a20d-c51b5b3184e2">GetThemePartSize</a> function to specify the type of size value to retrieve for a particular visual style part. 



