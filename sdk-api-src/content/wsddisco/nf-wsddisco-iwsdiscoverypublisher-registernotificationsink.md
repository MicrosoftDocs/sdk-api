---
UID: NF:wsddisco.IWSDiscoveryPublisher.RegisterNotificationSink
title: IWSDiscoveryPublisher::RegisterNotificationSink
author: windows-sdk-content
description: Attaches a callback notification sink to the discovery publisher.
old-location: ncd\iwsdiscoverypublisher_registernotificationsink_method.htm
old-project: WsdApi
ms.assetid: 75a6c593-298b-45b4-bde5-2a383b7581cc
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: IWSDiscoveryPublisher interface,RegisterNotificationSink method, IWSDiscoveryPublisher.RegisterNotificationSink, IWSDiscoveryPublisher::RegisterNotificationSink, RegisterNotificationSink, RegisterNotificationSink method, RegisterNotificationSink method,IWSDiscoveryPublisher interface, ncd.iwsdiscoverypublisher_registernotificationsink_method, wsddisco/IWSDiscoveryPublisher::RegisterNotificationSink
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wsddisco.h
req.include-header: Wsdapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wsddisco.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WSD_SECURITY_SIGNATURE_VALIDATION, *PWSD_SECURITY_SIGNATURE_VALIDATION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wsdapi.dll
api_name:
 - IWSDiscoveryPublisher.RegisterNotificationSink
product: Windows
targetos: Windows
req.lib: 
req.dll: Wsdapi.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWSDiscoveryPublisher::RegisterNotificationSink


## -description


Attaches a callback notification sink to the discovery publisher.


## -parameters




### -param pSink [in]

Pointer to an <a href="https://msdn.microsoft.com/6e7e0ab8-dffe-47c2-916c-a6734eb4ac44">IWSDiscoveryPublisherNotify</a> object that represents the initialized interface to receive callback notifications. This parameter cannot be <b>NULL</b>.


## -returns



Possible return values include, but are not limited to, the following:

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
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>pSink</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory to complete the operation.

</td>
</tr>
</table>
 




## -remarks



The notification sink receives a callback whenever an inbound query is received. It is possible to register multiple notification sinks with a single publisher.

<div class="alert"><b>Note</b>  <b>RegisterNotificationSink</b> must be called at least once before any other <a href="https://msdn.microsoft.com/4fff1328-d315-4a26-b7d8-43a273133e08">IWSDiscoveryPublisher</a> method is used.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/4fff1328-d315-4a26-b7d8-43a273133e08">IWSDiscoveryPublisher</a>
 

 

