---
UID: NF:tuner.IBDACreateTuneRequestEx.CreateTuneRequestEx
title: IBDACreateTuneRequestEx::CreateTuneRequestEx
author: windows-sdk-content
description: Creates a new tuning request for a tuning space. This method enables the caller to specify a particular type of tuning request.
old-location: mstv\ibdacreatetunerequestex_createtunerequestex.htm
tech.root: mstv
ms.assetid: bf378da2-be79-484e-84c6-bf1669b50218
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: CreateTuneRequestEx, CreateTuneRequestEx method [Microsoft TV Technologies], CreateTuneRequestEx method [Microsoft TV Technologies],IBDACreateTuneRequestEx interface, IBDACreateTuneRequestEx interface [Microsoft TV Technologies],CreateTuneRequestEx method, IBDACreateTuneRequestEx.CreateTuneRequestEx, IBDACreateTuneRequestEx::CreateTuneRequestEx, mstv.ibdacreatetunerequestex_createtunerequestex, tuner/IBDACreateTuneRequestEx::CreateTuneRequestEx
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: tuner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
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
 - IBDACreateTuneRequestEx.CreateTuneRequestEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IBDACreateTuneRequestEx::CreateTuneRequestEx


## -description


Creates a new tuning  request for a tuning space. This method enables the caller to specify a particular type of tuning request.


## -parameters




### -param TuneRequestIID [in]

GUID that identifies the type of <a href="https://msdn.microsoft.com/34077b45-32b4-466b-b103-6a42fc869265">ITuneRequest</a> object expected by the caller. If this value is <b>NULL</b>, this method behaves the same as <a href="https://msdn.microsoft.com/513d4d3e-47df-4a12-80ce-9fc1400af176">ITuningSpace::CreateTuneRequest</a> and creates an empty (uninitialized) <b>ITuneRequest</b> object.
          


### -param TuneRequest

TBD




#### - ppTuneRequest [out]

Address of a variable that receives a pointer to the <a href="https://msdn.microsoft.com/34077b45-32b4-466b-b103-6a42fc869265">ITuneRequest</a> interface of the new tuning request object. The caller must release the interface. If the <i>TuneRequestIID</i> argument is <b>NULL</b>, this address is set to <b>NULL</b> also.
          


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/b22ccd86-b8d7-4dd7-af4b-b99c9fea0de5">IBDACreateTuneRequestEx</a>



<a href="https://msdn.microsoft.com/513d4d3e-47df-4a12-80ce-9fc1400af176">ITuningSpace::CreateTuneRequest</a>
 

 

