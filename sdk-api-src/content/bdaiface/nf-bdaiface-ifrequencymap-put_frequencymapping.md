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

# IFrequencyMap::put_FrequencyMapping


## -description



The <b>put_FrequencyMapping</b> method sets the frequency table.




## -parameters




### -param ulCount [in]

Specifies the size of the array given in <i>pList</i>.


### -param pList [in]

Address of an array of size <i>ulCount</i>, allocated by the caller. The array should contain a list of all the frequencies (in kHz) that are valid in the current country/region.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -remarks



Applications can use this method to modify a frequency table or create new frequency tables. The changes are not stored by the Network Provider; the application must store the information itself and call <b>put_FrequencyMapping</b> each time the Network Provider is created.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/0f7f1b2c-a191-45f5-a645-367e898b6ee2">IFrequencyMap Interface</a>
 

 

