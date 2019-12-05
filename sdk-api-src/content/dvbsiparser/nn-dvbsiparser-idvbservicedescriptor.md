---
UID: NN:dvbsiparser.IDvbServiceDescriptor
title: IDvbServiceDescriptor (dvbsiparser.h)
description: Implements methods that get data from a Digital Video Broadcast (DVB) service descriptor.
old-location: mstv\idvbservicedescriptor.htm
tech.root: mstv
ms.assetid: 7024259f-3dcf-46e0-9984-d5924c9e5b54
ms.date: 12/05/2018
ms.keywords: IDvbServiceDescriptor, IDvbServiceDescriptor interface [Microsoft TV Technologies], IDvbServiceDescriptor interface [Microsoft TV Technologies],described, dvbsiparser/IDvbServiceDescriptor, mstv.idvbservicedescriptor
ms.topic: interface
f1_keywords:
- dvbsiparser/IDvbServiceDescriptor
dev_langs:
- c++
req.header: dvbsiparser.h
req.include-header: Dvbsiparser.idl
req.target-type: Windows
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
- IDvbServiceDescriptor
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDvbServiceDescriptor interface


## -description


Implements methods that get data from a Digital Video Broadcast (DVB) service descriptor.  The service  descriptor  appears in the DVB service information as part of the  service description table (SDT) or selection information table (SIT). It describes the service type and provides the names of the service provider and the service in text form.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDvbServiceDescriptor</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDvbServiceDescriptor</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDvbServiceDescriptor</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbservicedescriptor-getlength">GetLength</a>
</td>
<td align="left" width="63%">
Gets the body length from a DVB service descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbservicedescriptor-getprocessedservicename">GetProcessedServiceName</a>
</td>
<td align="left" width="63%">
Gets the processed service name from a DVB service descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbservicedescriptor-getservicename">GetServiceName</a>
</td>
<td align="left" width="63%">
Gets the service name from a DVB service descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbservicedescriptor-getservicenameemphasized">GetServiceNameEmphasized</a>
</td>
<td align="left" width="63%">
Gets the emphasized service name from a DVB service descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbservicedescriptor-getserviceprovidername">GetServiceProviderName</a>
</td>
<td align="left" width="63%">
Gets the service provider name from a DVB service descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbservicedescriptor-getserviceprovidernamew">GetServiceProviderNameW</a>
</td>
<td align="left" width="63%">
Gets the service provider name string from a DVB service descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbservicedescriptor-getservicetype">GetServiceType</a>
</td>
<td align="left" width="63%">
Gets the service type from a DVB service descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbservicedescriptor-gettag">GetTag</a>
</td>
<td align="left" width="63%">
Gets the identifying tag from a DVB service descriptor.

</td>
</tr>
</table> 

