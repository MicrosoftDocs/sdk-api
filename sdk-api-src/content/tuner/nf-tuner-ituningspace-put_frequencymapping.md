---
UID: NF:tuner.ITuningSpace.put_FrequencyMapping
title: ITuningSpace::put_FrequencyMapping method
author: windows-driver-content
description: The put_FrequencyMapping method creates a frequency/channel map, frequency/transponder map, or whatever other mapping from carrier frequencies to frequency identifiers is appropriate for the tuning space.
old-location: mstv\ituningspace_put_frequencymapping.htm
old-project: mstv
ms.assetid: 665ab139-773c-4e02-896f-2f97063a786f
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: ITuningSpace, ITuningSpace interface [Microsoft TV Technologies], put_FrequencyMapping method, ITuningSpace::put_FrequencyMapping, ITuningSpaceput_FrequencyMapping, mstv.ituningspace_put_frequencymapping, put_FrequencyMapping method [Microsoft TV Technologies], put_FrequencyMapping method [Microsoft TV Technologies], ITuningSpace interface, put_FrequencyMapping,ITuningSpace.put_FrequencyMapping, tuner/ITuningSpace::put_FrequencyMapping
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: tuner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Tuner.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: BITMAP_RENDERER_STATISTICS, *PBITMAP_RENDERER_STATISTICS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	tuner.h
api_name:
-	ITuningSpace.put_FrequencyMapping
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITuningSpace::put_FrequencyMapping method


## -description



The <b>put_FrequencyMapping</b> method creates a frequency/channel map, frequency/transponder map, or whatever other mapping from carrier frequencies to frequency identifiers is appropriate for the tuning space.




## -parameters




### -param Mapping [in]

<b>BSTR</b> that contains the frequency mappings.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -remarks



This method is used by the network provider to store a string that contains the frequency mappings.




## -see-also




<a href="https://msdn.microsoft.com/51850105-b3b1-4758-acde-05ca2f3439f2">ITuningSpace Interface</a>
 

 

