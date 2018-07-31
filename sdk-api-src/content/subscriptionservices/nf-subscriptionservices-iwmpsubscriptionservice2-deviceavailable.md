---
UID: NF:subscriptionservices.IWMPSubscriptionService2.deviceAvailable
title: IWMPSubscriptionService2::deviceAvailable
author: windows-sdk-content
description: Note  This section describes functionality designed for use by online stores.
old-location: wmp\iwmpsubscriptionservice2_deviceavailable.htm
old-project: WMP
ms.assetid: f3450e57-5e25-411c-8b21-b687021a6500
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IWMPSubscriptionService2 interface [Windows Media Player],deviceAvailable method, IWMPSubscriptionService2.deviceAvailable, IWMPSubscriptionService2::deviceAvailable, IWMPSubscriptionService2doMetering, deviceAvailable, deviceAvailable method [Windows Media Player], deviceAvailable method [Windows Media Player],IWMPSubscriptionService2 interface, subscriptionservices/IWMPSubscriptionService2::deviceAvailable, wmp.iwmpsubscriptionservice2_deviceavailable
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
 - IWMPSubscriptionService2.deviceAvailable
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IWMPSubscriptionService2::deviceAvailable


## -description



<div class="alert"><b>Note</b>  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported.</div>
<div> </div>
The <b>deviceAvailable</b> method is implemented by the online store to initiate device-specific processing tasks.




## -parameters




### -param bstrDeviceName [in]

String containing the device name.


### -param pCB [in]

Pointer to an <b>IWMPSubscriptionServiceCallback</b> interface. The online store uses this pointer to notify Windows Media Player that device-specific processing is complete.


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



Windows Media Player calls this method after a synchronization operation if the time elapsed since the last call is one week or more.

Your code should not perform lengthy operations synchronously when Windows Media Player calls this method. Instead, you must perform time-consuming tasks on a separate worker thread. When the worker thread has completed its work, it must call <a href="https://msdn.microsoft.com/1a6775b5-a909-49b1-98e8-ccc110294df6">IWMPSubscriptionServiceCallback::onComplete</a>.

Use the following procedure to provide your worker thread with a pointer to an <b>IWMPSubscriptionServiceCallback</b> interface.

<ol>
<li>Pass <i>pCB</i> to <b>CoMarshalInterThreadInterfaceInStream</b>, which returns an <b>IStream</b> pointer.</li>
<li>Pass the <b>IStream</b> pointer to your worker thread.</li>
<li>In your worker thread, call <b>CoGetInterfaceAndReleaseStream</b>, which returns an interface pointer that you can use to call <b>onComplete</b>.</li>
</ol>
The string contained in <i>bstrDeviceName</i> is not the same name retrieved by using <a href="https://msdn.microsoft.com/daa490a9-d7b8-4162-a4e2-f88b8f091fa3">IWMPSyncDevice::get_deviceName</a>. Rather, it is the canonical name retrieved by using the <b>IWMDMDevice2::GetCanonicalName</b> method provided by the Windows Media Device Manager SDK.




## -see-also




<a href="https://msdn.microsoft.com/5338a3c1-c44a-4c03-a21a-6cd5cfeef064">IWMPSubscriptionService2 Interface</a>



<a href="https://msdn.microsoft.com/c40d492e-030a-4e67-9199-09f44f39a507">IWMPSubscriptionServiceCallback Interface</a>
 

 

