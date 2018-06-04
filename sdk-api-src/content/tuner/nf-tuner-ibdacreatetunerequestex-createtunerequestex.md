---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# IBDACreateTuneRequestEx::CreateTuneRequestEx


## -description



      Creates a new tuning  request for a tuning space. This method enables the caller to specify a particular type of tuning request.


## -parameters




### -param TuneRequestIID [in]


            GUID that identifies the type of <a href="https://msdn.microsoft.com/34077b45-32b4-466b-b103-6a42fc869265">ITuneRequest</a> object expected by the caller. If this value is <b>NULL</b>, this method behaves the same as <a href="https://msdn.microsoft.com/513d4d3e-47df-4a12-80ce-9fc1400af176">ITuningSpace::CreateTuneRequest</a> and creates an empty (uninitialized) <b>ITuneRequest</b> object.
          


### -param TuneRequest






#### - ppTuneRequest [out]


            Address of a variable that receives a pointer to the <a href="https://msdn.microsoft.com/34077b45-32b4-466b-b103-6a42fc869265">ITuneRequest</a> interface of the new tuning request object. The caller must release the interface. If the <i>TuneRequestIID</i> argument is <b>NULL</b>, this address is set to <b>NULL</b> also.
          


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/b22ccd86-b8d7-4dd7-af4b-b99c9fea0de5">IBDACreateTuneRequestEx</a>



<a href="https://msdn.microsoft.com/513d4d3e-47df-4a12-80ce-9fc1400af176">ITuningSpace::CreateTuneRequest</a>
 

 

