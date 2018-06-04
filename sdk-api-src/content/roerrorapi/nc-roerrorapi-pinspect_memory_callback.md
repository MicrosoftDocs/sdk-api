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

# PINSPECT_MEMORY_CALLBACK callback function


## -description


Provides a function pointer to the callback used by the <a href="https://msdn.microsoft.com/2C5B04DD-888B-4400-A01D-CDF9DD870584">RoInspectCapturedStackBackTrace</a> function.


## -parameters




### -param *context [in]

Custom context data provided to the <a href="https://msdn.microsoft.com/2C5B04DD-888B-4400-A01D-CDF9DD870584">RoInspectCapturedStackBackTrace</a> function.


### -param readAddress [in]

The address to read data from.


### -param length [in]

The number of bytes to read, starting at <i>readAddress</i>. 


### -param *buffer [out]

The buffer that receives a copy of the bytes that are read.


## -returns



If this callback function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/2C5B04DD-888B-4400-A01D-CDF9DD870584">RoInspectCapturedStackBackTrace</a>
 

 

