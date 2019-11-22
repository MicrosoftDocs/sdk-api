---
UID: NN:dvbsiparser.IDvbLinkageDescriptor
title: IDvbLinkageDescriptor (dvbsiparser.h)

description: Defines methods that get data from a Digital Video Broadcast (DVB) linkage descriptor.
old-location: mstv\idvblinkagedescriptor.htm
tech.root: mstv
ms.assetid: 4e419b50-b9c2-48e4-a484-f0fcf5c9cb7f

ms.date: 12/05/2018
ms.keywords: IDvbLinkageDescriptor, IDvbLinkageDescriptor interface [Microsoft TV Technologies], IDvbLinkageDescriptor interface [Microsoft TV Technologies],described, dvbsiparser/IDvbLinkageDescriptor, mstv.idvblinkagedescriptor
ms.topic: interface
f1_keywords: 
 - "dvbsiparser/IDvbLinkageDescriptor"
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
 - IDvbLinkageDescriptor
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDvbLinkageDescriptor interface


## -description


Defines methods that get data from a Digital Video Broadcast (DVB) linkage descriptor. The linkage descriptor appears as part of the DVB service information in the network information table (NIT), bouquet association table (BAT), service description table (SDT), event information table (EIT), or service information table (SIT). 

The linkage descriptor identifies a service that can be presented if the consumer requests additional
information related to a service. The table that contains the linkage descriptor  indicates the entity for which additional information is available. For example, a linkage descriptor in the
NIT points to a service that provides additional information on the network, while a linkage descriptor in the BAT links to a service that provides information  about the bouquet.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDvbLinkageDescriptor</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDvbLinkageDescriptor</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDvbLinkageDescriptor</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvblinkagedescriptor-getlength">GetLength</a>
</td>
<td align="left" width="63%">
Gets the body length of a DVB linkage descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvblinkagedescriptor-getlinkagetype">GetLinkageType</a>
</td>
<td align="left" width="63%">
Gets a code that uniquely identifies the linkage type from a DVB linkage descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvblinkagedescriptor-getonid">GetONId</a>
</td>
<td align="left" width="63%">
Gets the network identifier of the  broadcast system that originates the information service from a DVB linkage descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvblinkagedescriptor-getprivatedata">GetPrivateData</a>
</td>
<td align="left" width="63%">
Gets the private data from a DVB linkage descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvblinkagedescriptor-getprivatedatalength">GetPrivateDataLength</a>
</td>
<td align="left" width="63%">
Gets the length of the private data field from a DVB linkage descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvblinkagedescriptor-getserviceid">GetServiceId</a>
</td>
<td align="left" width="63%">
Gets the identifier that identifies an information service a DVB linkage descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvblinkagedescriptor-gettag">GetTag</a>
</td>
<td align="left" width="63%">
Gets the tag that identifies a DVB linkage descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvblinkagedescriptor-gettsid">GetTSId</a>
</td>
<td align="left" width="63%">
Gets the identifier of the  transport stream that contains the information service from a DVB linkage descriptor.

</td>
</tr>
</table> 

