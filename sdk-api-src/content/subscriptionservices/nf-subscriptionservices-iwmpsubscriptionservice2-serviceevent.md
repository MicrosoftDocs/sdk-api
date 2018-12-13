---
UID: NF:subscriptionservices.IWMPSubscriptionService2.serviceEvent
title: IWMPSubscriptionService2::serviceEvent
author: windows-sdk-content
description: Note  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported. The serviceEvent method is called when the online store is activated or deactivated.
old-location: wmp\iwmpsubscriptionservice2_serviceevent.htm
tech.root: WMP
ms.assetid: 5937cf18-2548-45da-87eb-519448e64405
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWMPSubscriptionService2 interface [Windows Media Player],serviceEvent method, IWMPSubscriptionService2.serviceEvent, IWMPSubscriptionService2::serviceEvent, IWMPSubscriptionService2serviceEvent, serviceEvent, serviceEvent method [Windows Media Player], serviceEvent method [Windows Media Player],IWMPSubscriptionService2 interface, subscriptionservices/IWMPSubscriptionService2::serviceEvent, wmp.iwmpsubscriptionservice2_serviceevent
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - subscriptionservices.h
api_name:
 - IWMPSubscriptionService2.serviceEvent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMPSubscriptionService2::serviceEvent


## -description



<div class="alert"><b>Note</b>  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported.</div>
<div> </div>
The <b>serviceEvent</b> method is called when the online store is activated or deactivated.




## -parameters




### -param event [in]

A <a href="https://msdn.microsoft.com/9d04e534-083b-4227-82aa-4f7e50a492df">WMPSubscriptionServiceEvent</a> enumeration value indicating whether the service is activated or deactivated.


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



Your code should not perform lengthy operations synchronously when Windows Media Player calls this method. Instead, you must perform time-consuming tasks on a separate worker thread.




## -see-also




<a href="https://msdn.microsoft.com/5338a3c1-c44a-4c03-a21a-6cd5cfeef064">IWMPSubscriptionService2 Interface</a>



<a href="https://msdn.microsoft.com/9d04e534-083b-4227-82aa-4f7e50a492df">WMPSubscriptionServiceEvent</a>
 

 

