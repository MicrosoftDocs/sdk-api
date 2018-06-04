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

# enumCONFIDENCE_LEVEL enumeration


## -description



Indicates the level of confidence the recognizer has in the recognition result.




## -enum-fields




### -field CFL_STRONG

The recognizer is confident that the best alternate is correct.


### -field CFL_INTERMEDIATE

The recognizer is confident that the correct result is in the list of alternates.


### -field CFL_POOR

The recognizer is not confident that the result is in the list of alternates.

