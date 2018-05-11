---
UID: NF:tuner.ITuningSpace.get_FrequencyMapping
title: ITuningSpace::get_FrequencyMapping
author: windows-driver-content
description: The get_FrequencyMapping method retrieves the frequency mapping previously created by the network provider by a call to put_FrequencyMapping.
old-location: mstv\ituningspace_get_frequencymapping.htm
old-project: mstv
ms.assetid: 86f6f991-7ba6-4dcc-86bd-03e44c799c22
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: ITuningSpace interface [Microsoft TV Technologies],get_FrequencyMapping method, ITuningSpace.get_FrequencyMapping, ITuningSpace::get_FrequencyMapping, ITuningSpaceget_FrequencyMapping, get_FrequencyMapping, get_FrequencyMapping method [Microsoft TV Technologies], get_FrequencyMapping method [Microsoft TV Technologies],ITuningSpace interface, mstv.ituningspace_get_frequencymapping, tuner/ITuningSpace::get_FrequencyMapping
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
-	ITuningSpace.get_FrequencyMapping
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITuningSpace::get_FrequencyMapping


## -description



The <b>get_FrequencyMapping</b> method retrieves the frequency mapping previously created by the network provider by a call to <b>put_FrequencyMapping</b>.




## -parameters




### -param pMapping [out]

Pointer to a variable that receives the frequency mappings created by the Network Provider filter.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -remarks



The returned <b>BSTR</b> is treated as a binary blob. It is expected to contain embedded <b>NULL</b> values, and it may be formatted internally by the <a href="https://msdn.microsoft.com/f5de924f-defe-4300-a347-c9d63271dc90">BDA Network Provider</a>.

The caller must release the returned <b>BSTR</b> by calling <b>SysFreeString</b>.




## -see-also




<a href="https://msdn.microsoft.com/51850105-b3b1-4758-acde-05ca2f3439f2">ITuningSpace Interface</a>
 

 

