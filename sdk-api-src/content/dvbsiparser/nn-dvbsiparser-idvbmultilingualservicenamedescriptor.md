---
UID: NN:dvbsiparser.IDvbMultilingualServiceNameDescriptor
title: IDvbMultilingualServiceNameDescriptor (dvbsiparser.h)
description: Implements methods that get data from a Digital Video Broadcast (DVB) multilingual service name descriptor. A multilingual service name descriptor provides the names of the service provider and service in text form in one or more languages.
helpviewer_keywords: ["IDvbMultilingualServiceNameDescriptor","IDvbMultilingualServiceNameDescriptor interface [Microsoft TV Technologies]","IDvbMultilingualServiceNameDescriptor interface [Microsoft TV Technologies]","described","dvbsiparser/IDvbMultilingualServiceNameDescriptor","mstv.idvbmultilingualservicenamedescriptor"]
old-location: mstv\idvbmultilingualservicenamedescriptor.htm
tech.root: mstv
ms.assetid: 1b384ecf-aa56-476d-b347-b5438ab069fe
ms.date: 12/05/2018
ms.keywords: IDvbMultilingualServiceNameDescriptor, IDvbMultilingualServiceNameDescriptor interface [Microsoft TV Technologies], IDvbMultilingualServiceNameDescriptor interface [Microsoft TV Technologies],described, dvbsiparser/IDvbMultilingualServiceNameDescriptor, mstv.idvbmultilingualservicenamedescriptor
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDvbMultilingualServiceNameDescriptor
 - dvbsiparser/IDvbMultilingualServiceNameDescriptor
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dvbsiparser.h
api_name:
 - IDvbMultilingualServiceNameDescriptor
---

# IDvbMultilingualServiceNameDescriptor interface


## -description

Implements methods that get data from a Digital Video Broadcast (DVB) multilingual service name descriptor. A multilingual service name descriptor provides the names of the service provider and service in text
form in one or more languages.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDvbMultilingualServiceNameDescriptor</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDvbMultilingualServiceNameDescriptor</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDvbMultilingualServiceNameDescriptor</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbmultilingualservicenamedescriptor-getcountofrecords">GetCountOfRecords</a>
</td>
<td align="left" width="63%">
Gets the number of service names  from a DVB multilingual service name descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbmultilingualservicenamedescriptor-getlength">GetLength</a>
</td>
<td align="left" width="63%">
Gets the body length from a DVB multilingual service name descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbmultilingualservicenamedescriptor-getrecordlangid">GetRecordLangId</a>
</td>
<td align="left" width="63%">
 Gets the ISO 639 language code from a DVB multilingual service name descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbmultilingualservicenamedescriptor-getrecordservicenamew">GetRecordServiceNameW</a>
</td>
<td align="left" width="63%">
Gets the service name in string format  from a DVB multilingual service name descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbmultilingualservicenamedescriptor-getrecordserviceprovidernamew">GetRecordServiceProviderNameW</a>
</td>
<td align="left" width="63%">
 Gets the service provider name in string format from a DVB multilingual service name descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbmultilingualservicenamedescriptor-gettag">GetTag</a>
</td>
<td align="left" width="63%">
Gets the tag that identifies a DVB multilingual service name descriptor.

</td>
</tr>
</table>

