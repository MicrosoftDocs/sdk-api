---
UID: NF:bdaiface.IFrequencyMap.put_FrequencyMapping
title: IFrequencyMap::put_FrequencyMapping
author: windows-sdk-content
description: The put_FrequencyMapping method sets the frequency table.
old-location: mstv\ifrequencymap_put_frequencymapping.htm
old-project: mstv
ms.assetid: cfde2c8e-803d-46b8-b3d4-8e9b3129af0e
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IFrequencyMap interface [Microsoft TV Technologies],put_FrequencyMapping method, IFrequencyMap.put_FrequencyMapping, IFrequencyMap::put_FrequencyMapping, IFrequencyMapput_FrequencyMapping, bdaiface/IFrequencyMap::put_FrequencyMapping, mstv.ifrequencymap_put_frequencymapping, put_FrequencyMapping, put_FrequencyMapping method [Microsoft TV Technologies], put_FrequencyMapping method [Microsoft TV Technologies],IFrequencyMap interface
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
 - IFrequencyMap.put_FrequencyMapping
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
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
 

 

