---
UID: NF:segment.IMSVidTuner.get_Tune
title: IMSVidTuner::get_Tune
author: windows-sdk-content
description: The get_Tune method retrieves the current tune request.
old-location: mstv\imsvidtuner_get_tune.htm
tech.root: MSTV
ms.assetid: 189c878d-bf14-4464-96ce-5d2e09118dc4
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IMSVidTuner interface [Microsoft TV Technologies],get_Tune method, IMSVidTuner.get_Tune, IMSVidTuner::get_Tune, IMSVidTunerget_Tune, get_Tune, get_Tune method [Microsoft TV Technologies], get_Tune method [Microsoft TV Technologies],IMSVidTuner interface, mstv.imsvidtuner_get_tune, segment/IMSVidTuner::get_Tune
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - segment.h
api_name:
 - IMSVidTuner.get_Tune
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMSVidTuner::get_Tune


## -description


The <b>get_Tune</b> method retrieves the current tune request.


## -parameters




### -param ppTR [out]

Pointer to a variable that receives an <a href="https://msdn.microsoft.com/34077b45-32b4-466b-b103-6a42fc869265">ITuneRequest</a> interface pointer.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -remarks



The returned <a href="https://msdn.microsoft.com/34077b45-32b4-466b-b103-6a42fc869265">ITuneRequest</a> interface has an outstanding reference count. The caller must release the interface.




## -see-also




<a href="https://msdn.microsoft.com/b11f3ac4-c351-4017-9801-98d8edec7449">IMSVidTuner Interface</a>



<a href="https://msdn.microsoft.com/31139b6f-aad9-495b-9e8c-39026c8e81a9">IMSVidTuner::put_Tune</a>



<a href="https://msdn.microsoft.com/a0f36580-522f-48d6-989d-11e8d175ffdb">The Microsoft Unified Tuning Model</a>
 

 

