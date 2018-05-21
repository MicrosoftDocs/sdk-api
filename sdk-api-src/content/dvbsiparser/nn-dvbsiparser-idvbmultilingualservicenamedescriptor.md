---
UID: NN:dvbsiparser.IDvbMultilingualServiceNameDescriptor
title: IDvbMultilingualServiceNameDescriptor
author: windows-driver-content
description: Implements methods that get data from a Digital Video Broadcast (DVB) multilingual service name descriptor. A multilingual service name descriptor provides the names of the service provider and service in text form in one or more languages.
old-location: mstv\idvbmultilingualservicenamedescriptor.htm
old-project: mstv
ms.assetid: 1b384ecf-aa56-476d-b347-b5438ab069fe
ms.author: windowsdriverdev
ms.date: 5/14/2018
ms.keywords: IDvbMultilingualServiceNameDescriptor, IDvbMultilingualServiceNameDescriptor interface [Microsoft TV Technologies], IDvbMultilingualServiceNameDescriptor interface [Microsoft TV Technologies],described, dvbsiparser/IDvbMultilingualServiceNameDescriptor, mstv.idvbmultilingualservicenamedescriptor
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
req.typenames: DSROLE_UPGRADE_STATUS_INFO, *PDSROLE_UPGRADE_STATUS_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	dvbsiparser.h
api_name:
-	IDvbMultilingualServiceNameDescriptor
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDvbMultilingualServiceNameDescriptor interface


## -description


Implements methods that get data from a Digital Video Broadcast (DVB) multilingual service name descriptor. A multilingual service name descriptor provides the names of the service provider and service in text
form in one or more languages.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDvbMultilingualServiceNameDescriptor</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDvbMultilingualServiceNameDescriptor</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/c157e520-696f-45d8-8e43-0e6845882404">GetCountOfRecords</a>
</td>
<td align="left" width="63%">
Gets the number of service names  from a DVB multilingual service name descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/851d3d7b-0891-41a7-899e-61aac641ab3c">GetLength</a>
</td>
<td align="left" width="63%">
Gets the body length from a DVB multilingual service name descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a8432acb-f59b-4995-8b5d-576acab0f6b1">GetRecordLangId</a>
</td>
<td align="left" width="63%">
 Gets the ISO 639 language code from a DVB multilingual service name descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dfe9040d-18f1-4a35-a4ed-bb3f84ad8dd7">GetRecordServiceNameW</a>
</td>
<td align="left" width="63%">
Gets the service name in string format  from a DVB multilingual service name descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e07ebe5c-b5b3-4604-91c3-3e75042ad074">GetRecordServiceProviderNameW</a>
</td>
<td align="left" width="63%">
 Gets the service provider name in string format from a DVB multilingual service name descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/428f3309-67aa-4a47-9585-0308bee47e16">GetTag</a>
</td>
<td align="left" width="63%">
Gets the tag that identifies a DVB multilingual service name descriptor.

</td>
</tr>
</table> 

