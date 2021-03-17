---
UID: NF:wsddisco.IWSDiscoveryPublisher.RegisterNotificationSink
title: IWSDiscoveryPublisher::RegisterNotificationSink (wsddisco.h)
description: Attaches a callback notification sink to the discovery publisher.
helpviewer_keywords: ["IWSDiscoveryPublisher interface","RegisterNotificationSink method","IWSDiscoveryPublisher.RegisterNotificationSink","IWSDiscoveryPublisher::RegisterNotificationSink","RegisterNotificationSink","RegisterNotificationSink method","RegisterNotificationSink method","IWSDiscoveryPublisher interface","ncd.iwsdiscoverypublisher_registernotificationsink_method","wsddisco/IWSDiscoveryPublisher::RegisterNotificationSink"]
old-location: ncd\iwsdiscoverypublisher_registernotificationsink_method.htm
tech.root: ncd
ms.assetid: 75a6c593-298b-45b4-bde5-2a383b7581cc
ms.date: 12/05/2018
ms.keywords: IWSDiscoveryPublisher interface,RegisterNotificationSink method, IWSDiscoveryPublisher.RegisterNotificationSink, IWSDiscoveryPublisher::RegisterNotificationSink, RegisterNotificationSink, RegisterNotificationSink method, RegisterNotificationSink method,IWSDiscoveryPublisher interface, ncd.iwsdiscoverypublisher_registernotificationsink_method, wsddisco/IWSDiscoveryPublisher::RegisterNotificationSink
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWSDiscoveryPublisher::RegisterNotificationSink
 - wsddisco/IWSDiscoveryPublisher::RegisterNotificationSink
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wsdapi.dll
api_name:
 - IWSDiscoveryPublisher.RegisterNotificationSink
---

# IWSDiscoveryPublisher::RegisterNotificationSink


## -description

Attaches a callback notification sink to the discovery publisher.

## -parameters

### -param pSink [in]

Pointer to an <a href="/windows/desktop/api/wsddisco/nn-wsddisco-iwsdiscoverypublishernotify">IWSDiscoveryPublisherNotify</a> object that represents the initialized interface to receive callback notifications. This parameter cannot be <b>NULL</b>.

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

<div class="alert"><b>Note</b>  <b>RegisterNotificationSink</b> must be called at least once before any other <a href="/windows/desktop/api/wsddisco/nn-wsddisco-iwsdiscoverypublisher">IWSDiscoveryPublisher</a> method is used.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/wsddisco/nn-wsddisco-iwsdiscoverypublisher">IWSDiscoveryPublisher</a>