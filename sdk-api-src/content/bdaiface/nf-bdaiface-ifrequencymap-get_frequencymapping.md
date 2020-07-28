---
UID: NF:bdaiface.IFrequencyMap.get_FrequencyMapping
title: IFrequencyMap::get_FrequencyMapping (bdaiface.h)
description: The get_FrequencyMapping method returns the Network Provider filter's current frequency table.
helpviewer_keywords: ["IFrequencyMap interface [Microsoft TV Technologies]","get_FrequencyMapping method","IFrequencyMap.get_FrequencyMapping","IFrequencyMap::get_FrequencyMapping","IFrequencyMapget_FrequencyMapping","bdaiface/IFrequencyMap::get_FrequencyMapping","get_FrequencyMapping","get_FrequencyMapping method [Microsoft TV Technologies]","get_FrequencyMapping method [Microsoft TV Technologies]","IFrequencyMap interface","mstv.ifrequencymap_get_frequencymapping"]
old-location: mstv\ifrequencymap_get_frequencymapping.htm
tech.root: mstv
ms.assetid: 51fe636f-febe-4306-9c9a-7031a85440c6
ms.date: 12/05/2018
ms.keywords: IFrequencyMap interface [Microsoft TV Technologies],get_FrequencyMapping method, IFrequencyMap.get_FrequencyMapping, IFrequencyMap::get_FrequencyMapping, IFrequencyMapget_FrequencyMapping, bdaiface/IFrequencyMap::get_FrequencyMapping, get_FrequencyMapping, get_FrequencyMapping method [Microsoft TV Technologies], get_FrequencyMapping method [Microsoft TV Technologies],IFrequencyMap interface, mstv.ifrequencymap_get_frequencymapping
f1_keywords:
- bdaiface/IFrequencyMap.get_FrequencyMapping
dev_langs:
- c++
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- bdaiface.h
api_name:
- IFrequencyMap.get_FrequencyMapping
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFrequencyMap::get_FrequencyMapping


## -description



The <b>get_FrequencyMapping</b> method returns the Network Provider filter's current frequency table.




## -parameters




### -param ulCount [out]

Pointer to a variable that receives the size of the frequency table.


### -param ppulList [out]

Pointer to a variable that receives the address of the frequency table. The frequency table is an array of size <i>pulCount</i>, allocated by the method. The caller must free the array by calling <b>CoTaskMemFree</b>.


## -returns



Each entry in the frequency table is a tuning frequency, in kilohertz (kHz).

If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/bdaiface/nn-bdaiface-ifrequencymap">IFrequencyMap Interface</a>
 

 

