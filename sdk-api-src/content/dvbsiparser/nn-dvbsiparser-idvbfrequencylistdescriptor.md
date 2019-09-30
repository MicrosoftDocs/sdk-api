---
UID: NN:dvbsiparser.IDvbFrequencyListDescriptor
title: IDvbFrequencyListDescriptor (dvbsiparser.h)
author: windows-sdk-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
old-location: mstv\idvbfrequencylistdescriptor.htm
tech.root: mstv
ms.assetid: fadf7114-b9e4-4f61-816b-10725b83169a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDvbFrequencyListDescriptor, IDvbFrequencyListDescriptor interface [Microsoft TV Technologies], IDvbFrequencyListDescriptor interface [Microsoft TV Technologies],described, IDvbFrequencyListDescriptorInterface, dvbsiparser/IDvbFrequencyListDescriptor, mstv.idvbfrequencylistdescriptor
ms.topic: interface
f1_keywords: 
 - "dvbsiparser/IDvbFrequencyListDescriptor"
req.header: dvbsiparser.h
req.include-header: 
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
 - IDvbFrequencyListDescriptor
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDvbFrequencyListDescriptor interface


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        

The <b>IDvbFrequencyListDescriptor</b> interface enables the client to get a frequency list descriptor from a DVB stream. The frequency list descriptor may be present in the network information table (NIT). For more information, refer to ETSI EN 300 468.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDvbFrequencyListDescriptor</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDvbFrequencyListDescriptor</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDvbFrequencyListDescriptor</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbfrequencylistdescriptor-getcodingtype">GetCodingType</a>
</td>
<td align="left" width="63%">
Returns a flag that specifies how the frequency is coded.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbfrequencylistdescriptor-getcountofrecords">GetCountOfRecords</a>
</td>
<td align="left" width="63%">
Returns the number of records in the frequency list descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbfrequencylistdescriptor-getlength">GetLength</a>
</td>
<td align="left" width="63%">
Returns the length of the descriptor body.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbfrequencylistdescriptor-getrecordcentrefrequency">GetRecordCentreFrequency</a>
</td>
<td align="left" width="63%">
Returns the frequency at a specified index in the frequency list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbfrequencylistdescriptor-gettag">GetTag</a>
</td>
<td align="left" width="63%">
Returns the descriptor tag.

</td>
</tr>
</table> 


## -remarks



To obtain a pointer to this interface, do the following:

<ol>
<li>Call <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbsiparser-getnit">IDvbSiParser::GetNIT</a> to get the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvb_nit">IDVB_NIT</a> interface.</li>
<li>Call <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvb_nit-getrecorddescriptorbytag">IDVB_NIT::GetRecordDescriptorByTag</a> and pass in the frequency list descriptor tag (0x62). If the descriptor is present, the method returns an <a href="https://docs.microsoft.com/windows/desktop/api/mpeg2psiparser/nn-mpeg2psiparser-igenericdescriptor">IGenericDescriptor</a> pointer.</li>
<li>Query the returned <b>IGenericDescriptor</b> pointer for the <b>IDvbFrequencyListDescriptor</b> interface.</li>
</ol>



## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/bda-interfaces">BDA Interfaces</a>
 

 

