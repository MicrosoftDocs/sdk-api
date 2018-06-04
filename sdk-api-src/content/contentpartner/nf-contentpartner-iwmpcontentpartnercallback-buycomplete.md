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

# IWMPContentPartnerCallback::BuyComplete


## -description



<div class="alert"><b>Note</b>  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported.</div>
<div> </div>
The <b>BuyComplete</b> method notifies Windows Media Player that a purchase transaction has been completed.




## -parameters




### -param hrResult [in]

<b>HRESULT</b> return code indicating the success or failure of the transaction.


### -param dwBuyCookie [in]

The cookie that represents the purchase transaction. This value was provided when the Player called <a href="https://msdn.microsoft.com/a79c3d6e-b587-4bbc-b3bf-6489a54d71f9">IWMPContentPartner::Buy</a>.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
</table>
 




## -remarks



You must call <b>BuyComplete</b> exactly once for each call to <a href="https://msdn.microsoft.com/a79c3d6e-b587-4bbc-b3bf-6489a54d71f9">IWMPContentPartner::Buy</a>. Call <b>BuyComplete</b> when the transaction is finished, even if it failed for some reason.

Return a success code only after all licenses related to the purchase have been delivered.




## -see-also




<a href="https://msdn.microsoft.com/3c66052b-2b82-44aa-868d-5d5a4501c457">IWMPContentPartnerCallback Interface</a>
 

 

