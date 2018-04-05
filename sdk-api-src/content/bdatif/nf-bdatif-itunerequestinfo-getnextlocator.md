---
UID: NF:bdatif.ITuneRequestInfo.GetNextLocator
title: ITuneRequestInfo::GetNextLocator method
author: windows-driver-content
description: The GetNextLocator method creates a new tune request with locator information for the next transport stream on the network.
old-location: mstv\itunerequestinfo_getnextlocator.htm
old-project: mstv
ms.assetid: 300479bf-f8e3-41e2-898e-8a87e4abc801
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: GetNextLocator method [Microsoft TV Technologies], GetNextLocator method [Microsoft TV Technologies], ITuneRequestInfo interface, GetNextLocator,ITuneRequestInfo.GetNextLocator, ITuneRequestInfo, ITuneRequestInfo interface [Microsoft TV Technologies], GetNextLocator method, ITuneRequestInfo::GetNextLocator, ITuneRequestInfoGetNextLocator, bdatif/ITuneRequestInfo::GetNextLocator, mstv.itunerequestinfo_getnextlocator
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: bdatif.h
req.include-header: 
req.target-type: Windows
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
req.typenames: SpanningEventEmmMessage
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	bdatif.h
api_name:
-	ITuneRequestInfo.GetNextLocator
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ITuneRequestInfo::GetNextLocator method


## -description



The <b>GetNextLocator</b> method creates a new tune request with locator information for the next transport stream on the network.




## -parameters




### -param CurrentRequest




### -param TuneRequest






#### - pCurrentRequest [in]

Specifies the <a href="https://msdn.microsoft.com/34077b45-32b4-466b-b103-6a42fc869265">ITuneRequest</a> interface of the current tune request. <b>NULL</b> means to return information for the first stream.


#### - ppTuneRequest [out]

Pointer to a variable that receives a tune request for the next transport stream.


## -returns



The method returns an <b>HRESULT</b>. Possible values include those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>CurrentRequest</i> is not valid, or <i>TuneRequest</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



This method is used internally by the Network Provider's <a href="https://msdn.microsoft.com/43588b31-cac0-44c4-a282-b5939fed4ce7">IScanningTuner::SeekUp</a> and <a href="https://msdn.microsoft.com/ef78bae1-238f-4774-ab9a-b3681ba53656">IScanningTuner::SeekDown</a> methods, and is also useful for any Guide Store Loader that scans a network for EPG information.

Currently this method is not implemented for DVB-C or DVB-S networks, and the method returns E_NOTIMPL. The method is implemented for DVB-T.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/e5cb1a15-29c4-4e0f-aed2-eafe12ea007a">ITuneRequestInfo Interface</a>
 

 

