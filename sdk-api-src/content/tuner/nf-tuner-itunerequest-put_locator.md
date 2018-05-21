---
UID: NF:tuner.ITuneRequest.put_Locator
title: ITuneRequest::put_Locator
author: windows-driver-content
description: The put_Locator method is called from the Network Provider to set the ILocator object associated with the requested broadcast.
old-location: mstv\itunerequest_put_locator.htm
old-project: mstv
ms.assetid: 798ff904-5f08-4d3b-8a56-ca1c2df52aaf
ms.author: windowsdriverdev
ms.date: 5/14/2018
ms.keywords: ITuneRequest interface [Microsoft TV Technologies],put_Locator method, ITuneRequest.put_Locator, ITuneRequest::put_Locator, ITuneRequestput_Locator, mstv.itunerequest_put_locator, put_Locator, put_Locator method [Microsoft TV Technologies], put_Locator method [Microsoft TV Technologies],ITuneRequest interface, tuner/ITuneRequest::put_Locator
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
-	ITuneRequest.put_Locator
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITuneRequest::put_Locator


## -description



The <b>put_Locator</b> method is called from the Network Provider to set the <a href="https://msdn.microsoft.com/1d6c18f0-e7f1-4a1c-9edb-e4b66297becf">ILocator</a> object associated with the requested broadcast.




## -parameters




### -param Locator






#### - pLocator [in]

Pointer to an <b>ILocator</b> interface that specifies the new locator.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -see-also




<a href="https://msdn.microsoft.com/34077b45-32b4-466b-b103-6a42fc869265">ITuneRequest Interface</a>
 

 

