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

# IWMWriterPostView::GetReceivePostViewSamples


## -description



The <b>GetReceivePostViewSamples</b> method retrieves a flag indicating whether delivery of postview samples has been turned on for the specified stream.




## -parameters




### -param wStreamNum [in]

<b>WORD</b> containing the stream number.


### -param pfReceivePostViewSamples [out]

Pointer to a flag; True indicates that postview samples are to be delivered.


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
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
NULL value passed to <i>pfReceivePostViewSamples</i>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/1d24dbd6-86df-4a0a-8110-15f6a4c1f31d">IWMWriterPostView Interface</a>



<a href="https://msdn.microsoft.com/6d58671a-357b-412b-ad77-61866b0dcce3">IWMWriterPostView::SetReceivePostViewSamples</a>
 

 

