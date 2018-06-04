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

# D2D1_COLORMANAGEMENT_QUALITY enumeration


## -description


The quality level of the transform for the <a href="https://msdn.microsoft.com/7351C4B4-F289-4236-BB42-1B3BD8753248">Color management effect</a>. 


## -enum-fields




### -field D2D1_COLORMANAGEMENT_QUALITY_PROOF

The lowest quality mode. This mode requires feature level 9_1 or above.


### -field D2D1_COLORMANAGEMENT_QUALITY_NORMAL

Normal quality mode. This mode requires feature level 9_1 or above.


### -field D2D1_COLORMANAGEMENT_QUALITY_BEST

The best quality mode. This mode requires feature level 10_0 or above, as well as floating point precision buffers. 
          This mode supports floating point precision as well as extended range as defined in the ICC v4.3 specification. 


### -field D2D1_COLORMANAGEMENT_QUALITY_FORCE_DWORD



