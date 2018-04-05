---
UID: NF:segment.IMSVidTuner.put_Tune
title: IMSVidTuner::put_Tune method
author: windows-driver-content
description: The put_Tune method specifies the tune request.
old-location: mstv\imsvidtuner_put_tune.htm
old-project: mstv
ms.assetid: 31139b6f-aad9-495b-9e8c-39026c8e81a9
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: IMSVidTuner, IMSVidTuner interface [Microsoft TV Technologies], put_Tune method, IMSVidTuner::put_Tune, IMSVidTunerput_Tune, mstv.imsvidtuner_put_tune, put_Tune method [Microsoft TV Technologies], put_Tune method [Microsoft TV Technologies], IMSVidTuner interface, put_Tune,IMSVidTuner.put_Tune, segment/IMSVidTuner::put_Tune
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: segment.h
req.include-header: Msvidctl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Segment.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: SourceSizeList
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	segment.h
api_name:
-	IMSVidTuner.put_Tune
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IMSVidTuner::put_Tune method


## -description


The <a href="https://msdn.microsoft.com/69f71855-86d0-4ef9-a168-14e79461ec98">put_Tune</a> method specifies the tune request.


## -parameters




### -param pTR [in]

Specifies a pointer to the tune request's <a href="https://msdn.microsoft.com/34077b45-32b4-466b-b103-6a42fc869265">ITuneRequest</a> interface.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -see-also




<a href="https://msdn.microsoft.com/b11f3ac4-c351-4017-9801-98d8edec7449">IMSVidTuner Interface</a>



<a href="https://msdn.microsoft.com/189c878d-bf14-4464-96ce-5d2e09118dc4">IMSVidTuner::get_Tune</a>



<a href="https://msdn.microsoft.com/a0f36580-522f-48d6-989d-11e8d175ffdb">The Microsoft Unified Tuning Model</a>
 

 

