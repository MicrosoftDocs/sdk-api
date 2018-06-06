---
UID: NF:bdaiface.IFrequencyMap.get_FrequencyMapping
title: IFrequencyMap::get_FrequencyMapping
author: windows-sdk-content
description: The get_FrequencyMapping method returns the Network Provider filter's current frequency table.
old-location: mstv\ifrequencymap_get_frequencymapping.htm
old-project: mstv
ms.assetid: 51fe636f-febe-4306-9c9a-7031a85440c6
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IFrequencyMap interface [Microsoft TV Technologies],get_FrequencyMapping method, IFrequencyMap.get_FrequencyMapping, IFrequencyMap::get_FrequencyMapping, IFrequencyMapget_FrequencyMapping, bdaiface/IFrequencyMap::get_FrequencyMapping, get_FrequencyMapping, get_FrequencyMapping method [Microsoft TV Technologies], get_FrequencyMapping method [Microsoft TV Technologies],IFrequencyMap interface, mstv.ifrequencymap_get_frequencymapping
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: bdaiface.h
req.include-header: 
req.target-type: Windows
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
tech.root: 
req.typenames: UICloseReasonType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - bdaiface.h
api_name:
 - IFrequencyMap.get_FrequencyMapping
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IFrequencyMap::get_FrequencyMapping


## -description



The <b>get_FrequencyMapping</b> method returns the Network Provider filter's current frequency table.




## -parameters




### -param ulCount




### -param ppulList [out]

Pointer to a variable that receives the address of the frequency table. The frequency table is an array of size <i>pulCount</i>, allocated by the method. The caller must free the array by calling <b>CoTaskMemFree</b>.


#### - pulCount [out]

Pointer to a variable that receives the size of the frequency table.


## -returns



Each entry in the frequency table is a tuning frequency, in kilohertz (kHz).

If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/0f7f1b2c-a191-45f5-a645-367e898b6ee2">IFrequencyMap Interface</a>
 

 

