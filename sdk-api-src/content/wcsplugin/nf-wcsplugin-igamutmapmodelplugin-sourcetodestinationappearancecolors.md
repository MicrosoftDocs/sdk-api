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

# IGamutMapModelPlugIn::SourceToDestinationAppearanceColors


## -description


Returns the appropriate gamut-mapped appearance colors in response to the specified number of colors and the <a href="wcs.IGamutMapModelPlugIn::SourceToDestinationAppearanceColors">CIEJCh</a> colors.


## -parameters




### -param cColors [in]

The number of colors in the <i>pXYZColors</i> and <i>pDeviceValues</i> arrays.


### -param pInputColors [in]

A pointer to the array of incoming colors to be gamut mapped.


### -param pOutputColors [out]

A pointer to the array of outgoing colors.


## -returns



If this function succeeds, the return value is S_OK.

If this function fails, the return value is E_FAIL.




## -see-also




<a href="https://msdn.microsoft.com/a0623917-0b63-4546-a71a-1e9efa9fe8e5">Basic Color Management Concepts</a>



<a href="https://msdn.microsoft.com/794eb94c-fdb3-42b3-8320-b13bf51324d1">IGamutMapModelPlugIn</a>
 

 

