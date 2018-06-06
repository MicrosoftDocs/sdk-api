---
UID: NF:subscriptionservices.IWMPSubscriptionServiceCallback.onComplete
title: IWMPSubscriptionServiceCallback::onComplete
author: windows-sdk-content
description: Note  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported. The onComplete method notifies Windows Media Player when a background process is completed.
old-location: wmp\iwmpsubscriptionservicecallback_oncomplete.htm
old-project: WMP
ms.assetid: 1a6775b5-a909-49b1-98e8-ccc110294df6
ms.author: windowssdkdev
ms.date: 05/04/2018
ms.keywords: IWMPSubscriptionServiceCallback interface [Windows Media Player],onComplete method, IWMPSubscriptionServiceCallback.onComplete, IWMPSubscriptionServiceCallback::onComplete, IWMPSubscriptionServiceCallbackonComplete, onComplete, onComplete method [Windows Media Player], onComplete method [Windows Media Player],IWMPSubscriptionServiceCallback interface, subscriptionservices/IWMPSubscriptionServiceCallback::onComplete, wmp.iwmpsubscriptionservicecallback_oncomplete
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: subscriptionservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Media Player 10 or later.
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
tech.root: 
req.typenames: WMPSubscriptionServiceEvent
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - subscriptionservices.h
api_name:
 - IWMPSubscriptionServiceCallback.onComplete
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
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
 

 

