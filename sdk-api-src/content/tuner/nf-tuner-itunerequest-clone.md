---
UID: NF:tuner.ITuneRequest.Clone
title: ITuneRequest::Clone
author: windows-sdk-content
description: The Clone method returns a new copy of this tune request.
old-location: mstv\itunerequest_clone.htm
tech.root: mstv
ms.assetid: 14298e56-805d-48f3-9f78-79d4eaf2239f
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: Clone, Clone method [Microsoft TV Technologies], Clone method [Microsoft TV Technologies],ITuneRequest interface, ITuneRequest interface [Microsoft TV Technologies],Clone method, ITuneRequest.Clone, ITuneRequest::Clone, ITuneRequestClone, mstv.itunerequest_clone, tuner/ITuneRequest::Clone
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
 - ITuneRequest.Clone
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITuneRequest::Clone


## -description



The <b>Clone</b> method returns a new copy of this tune request.




## -parameters




### -param NewTuneRequest

TBD




#### - ppNewTuneRequest [out]

Address of an <b>ITuneRequest</b> interface pointer that will be set to the new object.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -remarks



This method performs a "deep copy" of the object; in other words it copies all sub-objects as well, including <a href="https://msdn.microsoft.com/6d779095-12f9-4e00-a25f-0a840f5149fa">Components</a>, <a href="https://msdn.microsoft.com/d1601651-84a2-4fd8-9318-653aa569e747">LanguageComponentType</a> objects, and so on.




## -see-also




<a href="https://msdn.microsoft.com/34077b45-32b4-466b-b103-6a42fc869265">ITuneRequest Interface</a>
 

 

