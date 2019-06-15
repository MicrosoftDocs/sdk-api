---
UID: NF:tuner.ITuningSpace.CreateTuneRequest
title: ITuningSpace::CreateTuneRequest (tuner.h)
author: windows-sdk-content
description: The CreateTuneRequest method creates an empty (uninitialized) tune request.
old-location: mstv\ituningspace_createtunerequest.htm
tech.root: mstv
ms.assetid: 513d4d3e-47df-4a12-80ce-9fc1400af176
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CreateTuneRequest, CreateTuneRequest method [Microsoft TV Technologies], CreateTuneRequest method [Microsoft TV Technologies],ITuningSpace interface, ITuningSpace interface [Microsoft TV Technologies],CreateTuneRequest method, ITuningSpace.CreateTuneRequest, ITuningSpace::CreateTuneRequest, ITuningSpaceCreateTuneRequest, mstv.ituningspace_createtunerequest, tuner/ITuningSpace::CreateTuneRequest
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tuner.h
api_name:
 - ITuningSpace.CreateTuneRequest
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITuningSpace::CreateTuneRequest


## -description



The <b>CreateTuneRequest</b> method creates an empty (uninitialized) tune request.




## -parameters




### -param TuneRequest [out]

Address of a variable that receives a pointer to the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nn-tuner-itunerequest">ITuneRequest</a> interface of the new tune request object. The caller must release the interface.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -remarks



You can query the returned <b>ITuneRequest</b> pointer for derived interfaces. For more information, see the reference pages for the individual tuning space objects, which are listed in the topic <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/tuning-model-objects">Tuning Model Objects</a>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nn-tuner-ituningspace">ITuningSpace Interface</a>
 

 

