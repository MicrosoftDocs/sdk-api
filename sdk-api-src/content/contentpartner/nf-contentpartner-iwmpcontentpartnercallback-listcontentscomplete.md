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

# IWMPContentPartnerCallback::ListContentsComplete


## -description



<div class="alert"><b>Note</b>  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported.</div>
<div> </div>
The <b>ListContentsComplete</b> method notifies Windows Media Player that the content partner plug-in is finished adding content to a list.




## -parameters




### -param dwListCookie [in]

A cookie that identifies a list retrieval session. Windows Media Player previously supplied this cookie to the content partner plug-in by calling <a href="https://msdn.microsoft.com/a48935ea-8275-4b68-a1ab-006a23c455ad">IWMPContentPartner::GetListContents</a>.


### -param hrSuccess [in]

An <b>HRESULT</b> that indicates whether the overall transfer of list contents succeeded. Any success code indicates that the transfer succeeded; any error code indicates that the transfer failed.


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



Windows Media Player starts retrieving list contents by calling <a href="https://msdn.microsoft.com/a48935ea-8275-4b68-a1ab-006a23c455ad">IWMPContentPartner::GetListContents</a>. This starts an asynchronous operation in which the online store plug-in must call <a href="https://msdn.microsoft.com/22d28495-310e-4f3d-a0e3-8f6679c78c40">IWMPContentPartnerCallback::AddListContents</a> one or more times to give the Player the requested data. The plug-in must finally call <b>ListContentsComplete</b> to notify the Player that all the data has been provided.




## -see-also




<a href="https://msdn.microsoft.com/3c66052b-2b82-44aa-868d-5d5a4501c457">IWMPContentPartnerCallback Interface</a>
 

 

