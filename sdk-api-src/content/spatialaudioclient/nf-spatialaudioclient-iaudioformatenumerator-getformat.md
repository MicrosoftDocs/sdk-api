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

# IAudioFormatEnumerator::GetFormat


## -description


Gets the format with the specified index in the list. The formats are listed in order of importance. The most preferable format is first in the list.


## -parameters




### -param index [in]

The index of the item in the list to retrieve.


### -param format [out]

Pointer to a pointer to a <b>WAVEFORMATEX</b> structure describing a supported audio format.


## -returns



If the method succeeds, it returns S_OK.




## -see-also




<a href="https://msdn.microsoft.com/50434617-E70E-4931-B98E-61650E9DEA7E">IAudioFormatEnumerator</a>
 

 

