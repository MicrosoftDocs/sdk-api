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

# IWMPSubscriptionServiceCallback::onComplete


## -description



<div class="alert"><b>Note</b>  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported.</div>
<div> </div>
The <b>onComplete</b> method notifies Windows Media Player when a background process is completed.




## -parameters




### -param hrResult [in]

<b>HRESULT</b> success or error code.


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




<a href="https://msdn.microsoft.com/64ab5548-b562-44e4-9798-8f14d3ed653b">IWMPSubscriptionService2::prepareForSync</a> and <a href="https://msdn.microsoft.com/f3450e57-5e25-411c-8b21-b687021a6500">IWMPSubscriptionService2::deviceAvailable</a> supply a pointer to an <b>IWMPSubscriptionServiceCallback</b> interface. When responding to calls from Windows Media Player to these methods, you must pass any time-consuming tasks to a separate worker thread and return immediately. When the worker thread has completed its task, it must call <b>IWMPSubscriptionServiceCallback::onComplete</b>.

In your <b>prepareForSync</b> and <b>deviceAvailable</b> methods, use the following procedure to provide your worker thread with a pointer to an <b>IWMPSubscriptionServiceCallback</b> interface.

<ol>
<li>Pass the pointer supplied in the <i>pCB</i> parameter to <b>CoMarshalInterThreadInterfaceInStream</b>, which returns an <b>IStream</b> pointer.</li>
<li>Pass the <b>IStream</b> pointer to your worker thread.</li>
<li>In your worker thread, call <b>CoGetInterfaceAndReleaseStream</b>, which returns an interface pointer that you can use to call <b>onComplete</b>.</li>
</ol>



## -see-also




<a href="https://msdn.microsoft.com/c40d492e-030a-4e67-9199-09f44f39a507">IWMPSubscriptionServiceCallback Interface</a>
 

 

