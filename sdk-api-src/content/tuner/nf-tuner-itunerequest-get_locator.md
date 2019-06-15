---
UID: NF:tuner.ITuneRequest.get_Locator
title: ITuneRequest::get_Locator (tuner.h)
author: windows-sdk-content
description: The get_Locator method is called from the Network Provider to get the ILocator object associated with the requested broadcast.
old-location: mstv\itunerequest_get_locator.htm
tech.root: mstv
ms.assetid: 9f2a000a-0133-44f4-8e9c-7d37435596d7
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITuneRequest interface [Microsoft TV Technologies],get_Locator method, ITuneRequest.get_Locator, ITuneRequest::get_Locator, ITuneRequestget_Locator, get_Locator, get_Locator method [Microsoft TV Technologies], get_Locator method [Microsoft TV Technologies],ITuneRequest interface, mstv.itunerequest_get_locator, tuner/ITuneRequest::get_Locator
ms.topic: method
f1_keywords: ["tuner/ITuneRequest.get_Locator"]
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
 - ITuneRequest.get_Locator
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITuneRequest::get_Locator


## -description



The <b>get_Locator</b> method is called from the Network Provider to get the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nn-tuner-ilocator">ILocator</a> object associated with the requested broadcast.




## -parameters




### -param Locator [out]

Address of an <b>ILocator</b> interface pointer that will be set to the new object.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nn-tuner-itunerequest">ITuneRequest Interface</a>
 

 

