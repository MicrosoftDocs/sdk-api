---
UID: NF:tuner.ITuneRequest.get_TuningSpace
title: ITuneRequest::get_TuningSpace
author: windows-sdk-content
description: The get_TuningSpace method retrieves the tuning space that was used to create this tune request.
old-location: mstv\itunerequest_get_tuningspace.htm
old-project: mstv
ms.assetid: 6952df72-30f3-4c33-a0bf-d2ad8022042c
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: ITuneRequest interface [Microsoft TV Technologies],get_TuningSpace method, ITuneRequest.get_TuningSpace, ITuneRequest::get_TuningSpace, ITuneRequestget_TuningSpace, get_TuningSpace, get_TuningSpace method [Microsoft TV Technologies], get_TuningSpace method [Microsoft TV Technologies],ITuneRequest interface, mstv.itunerequest_get_tuningspace, tuner/ITuneRequest::get_TuningSpace
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: tuner.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: BITMAP_RENDERER_STATISTICS, *PBITMAP_RENDERER_STATISTICS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tuner.h
api_name:
 - ITuneRequest.get_TuningSpace
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITuneRequest::get_TuningSpace


## -description



The <b>get_TuningSpace</b> method retrieves the tuning space that was used to create this tune request.




## -parameters




### -param TuningSpace






#### - ppTuningSpace [out]

Receives a pointer to the <a href="https://msdn.microsoft.com/51850105-b3b1-4758-acde-05ca2f3439f2">ITuningSpace</a> interface. The caller must release the interface.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -remarks



You must first access the tuning space in order to obtain the default locator and the default preferred component types.




## -see-also




<a href="https://msdn.microsoft.com/34077b45-32b4-466b-b103-6a42fc869265">ITuneRequest Interface</a>
 

 

