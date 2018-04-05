---
UID: NF:tuner.IDVBSTuningSpace.get_InputRange
title: IDVBSTuningSpace::get_InputRange method
author: windows-driver-content
description: The get_InputRange method retrieves an integer indicating which option or switch contains the requested signal source.
old-location: mstv\idvbstuningspace_get_inputrange.htm
old-project: mstv
ms.assetid: d116c1d1-df48-434b-ad49-eabd0efaa810
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: IDVBSTuningSpace, IDVBSTuningSpace interface [Microsoft TV Technologies], get_InputRange method, IDVBSTuningSpace::get_InputRange, IDVBSTuningSpaceget_InputRange, get_InputRange method [Microsoft TV Technologies], get_InputRange method [Microsoft TV Technologies], IDVBSTuningSpace interface, get_InputRange,IDVBSTuningSpace.get_InputRange, mstv.idvbstuningspace_get_inputrange, tuner/IDVBSTuningSpace::get_InputRange
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
-	IDVBSTuningSpace.get_InputRange
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IDVBSTuningSpace::get_InputRange method


## -description



The <b>get_InputRange</b> method retrieves an integer indicating which option or switch contains the requested signal source.




## -parameters




### -param InputRange






#### - pInputRange [out]

Receives the input range.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -see-also




<a href="https://msdn.microsoft.com/46c143d7-b9ec-4808-a4d2-337e6e0252dd">IDVBSTuningSpace Interface</a>
 

 

