---
UID: NF:tuner.ITuneRequest.get_Locator
title: ITuneRequest::get_Locator
author: windows-sdk-content
description: The get_Locator method is called from the Network Provider to get the ILocator object associated with the requested broadcast.
old-location: mstv\itunerequest_get_locator.htm
old-project: mstv
ms.assetid: 9f2a000a-0133-44f4-8e9c-7d37435596d7
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: ITuneRequest interface [Microsoft TV Technologies],get_Locator method, ITuneRequest.get_Locator, ITuneRequest::get_Locator, ITuneRequestget_Locator, get_Locator, get_Locator method [Microsoft TV Technologies], get_Locator method [Microsoft TV Technologies],ITuneRequest interface, mstv.itunerequest_get_locator, tuner/ITuneRequest::get_Locator
ms.prod: windows
ms.technology: windows-sdk
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
 - ITuneRequest.get_Locator
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITuneRequest::get_Locator


## -description



The <b>get_Locator</b> method is called from the Network Provider to get the <a href="https://msdn.microsoft.com/1d6c18f0-e7f1-4a1c-9edb-e4b66297becf">ILocator</a> object associated with the requested broadcast.




## -parameters




### -param Locator






#### - ppLocator [out]

Address of an <b>ILocator</b> interface pointer that will be set to the new object.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -see-also




<a href="https://msdn.microsoft.com/34077b45-32b4-466b-b103-6a42fc869265">ITuneRequest Interface</a>
 

 

