---
UID: NF:tuner.IDVBTuneRequest.get_SID
title: IDVBTuneRequest::get_SID method
author: windows-driver-content
description: The get_SID method retrieves the service ID for the network.
old-location: mstv\idvbtunerequest_get_sid.htm
old-project: mstv
ms.assetid: 2ddd5eec-c8bc-4f26-8acd-cf42876345ad
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: IDVBTuneRequest, IDVBTuneRequest interface [Microsoft TV Technologies], get_SID method, IDVBTuneRequest::get_SID, IDVBTuneRequestget_SID, get_SID method [Microsoft TV Technologies], get_SID method [Microsoft TV Technologies], IDVBTuneRequest interface, get_SID,IDVBTuneRequest.get_SID, mstv.idvbtunerequest_get_sid, tuner/IDVBTuneRequest::get_SID
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
-	IDVBTuneRequest.get_SID
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IDVBTuneRequest::get_SID method


## -description



The <b>get_SID</b> method retrieves the service ID for the network.




## -parameters




### -param SID






#### - pSID [out]

Receives the service ID.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -see-also




<a href="https://msdn.microsoft.com/4d519bbc-38e1-47ce-bd73-a3eb1ea399d6">IDVBTuneRequest Interface</a>
 

 

