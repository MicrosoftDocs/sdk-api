---
UID: NF:tuner.ITuningSpace.CreateTuneRequest
title: ITuningSpace::CreateTuneRequest
author: windows-driver-content
description: The CreateTuneRequest method creates an empty (uninitialized) tune request.
old-location: mstv\ituningspace_createtunerequest.htm
old-project: mstv
ms.assetid: 513d4d3e-47df-4a12-80ce-9fc1400af176
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: CreateTuneRequest, CreateTuneRequest method [Microsoft TV Technologies], CreateTuneRequest method [Microsoft TV Technologies],ITuningSpace interface, ITuningSpace interface [Microsoft TV Technologies],CreateTuneRequest method, ITuningSpace.CreateTuneRequest, ITuningSpace::CreateTuneRequest, ITuningSpaceCreateTuneRequest, mstv.ituningspace_createtunerequest, tuner/ITuningSpace::CreateTuneRequest
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
-	ITuningSpace.CreateTuneRequest
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITuningSpace::CreateTuneRequest


## -description



The <b>CreateTuneRequest</b> method creates an empty (uninitialized) tune request.




## -parameters




### -param TuneRequest






#### - ppTuneRequest [out]

Address of a variable that receives a pointer to the <a href="https://msdn.microsoft.com/34077b45-32b4-466b-b103-6a42fc869265">ITuneRequest</a> interface of the new tune request object. The caller must release the interface.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -remarks



You can query the returned <b>ITuneRequest</b> pointer for derived interfaces. For more information, see the reference pages for the individual tuning space objects, which are listed in the topic <a href="https://msdn.microsoft.com/cf6a81cd-a955-4816-a43e-85138ecd8246">Tuning Model Objects</a>.




## -see-also




<a href="https://msdn.microsoft.com/51850105-b3b1-4758-acde-05ca2f3439f2">ITuningSpace Interface</a>
 

 

