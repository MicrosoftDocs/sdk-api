---
UID: NF:tuner.IMPEG2TuneRequestFactory.CreateTuneRequest
title: IMPEG2TuneRequestFactory::CreateTuneRequest
author: windows-sdk-content
description: The CreateTuneRequest method creates the minimal MPEG-2 tune request for a specified tuning space.
old-location: mstv\impeg2tunerequestfactory_createtunerequest.htm
tech.root: MSTV
ms.assetid: 41e299d6-492e-40b4-955f-603b18da0c02
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: CreateTuneRequest, CreateTuneRequest method [Microsoft TV Technologies], CreateTuneRequest method [Microsoft TV Technologies],IMPEG2TuneRequestFactory interface, IMPEG2TuneRequestFactory interface [Microsoft TV Technologies],CreateTuneRequest method, IMPEG2TuneRequestFactory.CreateTuneRequest, IMPEG2TuneRequestFactory::CreateTuneRequest, IMPEG2TuneRequestFactoryCreateTuneRequest, mstv.impeg2tunerequestfactory_createtunerequest, tuner/IMPEG2TuneRequestFactory::CreateTuneRequest
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: tuner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
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
 - IMPEG2TuneRequestFactory.CreateTuneRequest
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMPEG2TuneRequestFactory::CreateTuneRequest


## -description


The <b>CreateTuneRequest</b> method creates the minimal MPEG-2 tune request for a specified tuning space.


## -parameters




### -param TuningSpace [in]

Pointer to the <a href="https://msdn.microsoft.com/51850105-b3b1-4758-acde-05ca2f3439f2">ITuningSpace</a> interface of the tuning space.


### -param TuneRequest [out]

Address of a variable that receives a pointer to the <a href="https://msdn.microsoft.com/a9e37b8b-9272-43c6-b36e-1e82b0d1b0db">IMPEG2TuneRequest</a> interface.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -see-also




<a href="https://msdn.microsoft.com/0fbeab7d-0c54-45e3-a73c-755df28a16d5">IMPEG2TuneRequestFactory Interface</a>
 

 

