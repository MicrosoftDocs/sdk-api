---
UID: NN:dvbsiparser.IDvbServiceDescriptor2
title: IDvbServiceDescriptor2 (dvbsiparser.h)
description: Implements methods that get the string values from fields in a Digital Video Broadcast (DVB) service descriptor. The service descriptor describes the service type, and provides the names of the service provider and the service in text form.
old-location: mstv\idvbservicedescriptor2.htm
tech.root: mstv
ms.assetid: 795c4a5c-c363-401b-8b26-447903163f80
ms.date: 12/05/2018
ms.keywords: IDvbServiceDescriptor2, IDvbServiceDescriptor2 interface [Microsoft TV Technologies], IDvbServiceDescriptor2 interface [Microsoft TV Technologies],described, dvbsiparser/IDvbServiceDescriptor2, mstv.idvbservicedescriptor2
f1_keywords:
- dvbsiparser/IDvbServiceDescriptor2
dev_langs:
- c++
req.header: dvbsiparser.h
req.include-header: Dvbsiparser.idl
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
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
- dvbsiparser.h
api_name:
- IDvbServiceDescriptor2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDvbServiceDescriptor2 interface


## -description


Implements methods that get the string values from fields in a Digital Video Broadcast (DVB) service descriptor. The service descriptor describes the service type, and provides the names of the service provider and the service in text form.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDvbServiceDescriptor2</b> interface inherits from <b>IDvbServiceDescriptor</b>. <b>IDvbServiceDescriptor2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDvbServiceDescriptor2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbservicedescriptor2-getservicenamew">GetServiceNameW</a>
</td>
<td align="left" width="63%">
Gets the service name from the DVB service descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbservicedescriptor2-getserviceprovidernamew">GetServiceProviderNameW</a>
</td>
<td align="left" width="63%">
Gets the service provider name from the DVB service descriptor.

</td>
</tr>
</table> 

