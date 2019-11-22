---
UID: NF:wsddisco.IWSDiscoveryPublisher.UnRegisterNotificationSink
title: IWSDiscoveryPublisher::UnRegisterNotificationSink (wsddisco.h)

description: Detaches a callback notification sink from the discovery publisher.
old-location: ncd\iwsdiscoverypublisher_unregisternotificationsink_method.htm
tech.root: WsdApi
ms.assetid: aaf6bc07-8ce9-41f7-b468-971b31b51a86

ms.date: 12/05/2018
ms.keywords: IWSDiscoveryPublisher interface,UnRegisterNotificationSink method, IWSDiscoveryPublisher.UnRegisterNotificationSink, IWSDiscoveryPublisher::UnRegisterNotificationSink, UnRegisterNotificationSink, UnRegisterNotificationSink method, UnRegisterNotificationSink method,IWSDiscoveryPublisher interface, ncd.iwsdiscoverypublisher_unregisternotificationsink_method, wsddisco/IWSDiscoveryPublisher::UnRegisterNotificationSink
ms.topic: method
f1_keywords: 
 - "wsddisco/IWSDiscoveryPublisher.UnRegisterNotificationSink"
dev_langs:
 - c++
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
req.lib: 
req.dll: Wsdapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wsdapi.dll
api_name:
 - IWSDiscoveryPublisher.UnRegisterNotificationSink
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWSDiscoveryPublisher::UnRegisterNotificationSink


## -description


Detaches a callback notification sink from the discovery publisher.


## -parameters




### -param pSink [in]

Pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/wsddisco/nn-wsddisco-iwsdiscoverypublishernotify">IWSDiscoveryPublisherNotify</a> interface that will stop receiving callback notifications.


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
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The method failed.

</td>
</tr>
</table>
 




## -remarks



<div class="alert"><b>Note</b>  <b>UnRegisterNotificationSink</b> must be called at least once for each notification sink previously attached to the discovery publisher.</div>
<div> </div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wsddisco/nn-wsddisco-iwsdiscoverypublisher">IWSDiscoveryPublisher</a>
 

 

