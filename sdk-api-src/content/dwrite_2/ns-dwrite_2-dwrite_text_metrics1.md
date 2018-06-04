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

# DWRITE_TEXT_METRICS1 structure


## -description


Contains the metrics associated with text after layout.
        All coordinates are in device independent pixels (DIPs).
      

<b>DWRITE_TEXT_METRICS1</b> extends <a href="https://msdn.microsoft.com/4524ace3-fca6-4daf-9ecb-516771e53fc9">DWRITE_TEXT_METRICS</a> 
        to include the height of the formatted text.
      


## -struct-fields




### -field heightIncludingTrailingWhitespace

The height of the formatted text taking into account the trailing whitespace at the end of each line. This is
            pertinent for vertical text.


### -field DWRITE_TEXT_METRICS

 



