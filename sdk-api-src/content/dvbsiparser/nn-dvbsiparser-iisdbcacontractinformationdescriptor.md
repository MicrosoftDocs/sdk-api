---
UID: NN:dvbsiparser.IIsdbCAContractInformationDescriptor
title: IIsdbCAContractInformationDescriptor (dvbsiparser.h)
author: windows-sdk-content
description: Implements methods that get data from an Integrated Services Digital Broadcasting (ISDB) conditional access (CA) contract information descriptor.
old-location: mstv\iisdbcacontractinformationdescriptor.htm
tech.root: mstv
ms.assetid: d877a625-d683-4472-98de-f24c165c753a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IIsdbCAContractInformationDescriptor, IIsdbCAContractInformationDescriptor interface [Microsoft TV Technologies], IIsdbCAContractInformationDescriptor interface [Microsoft TV Technologies],described, dvbsiparser/IIsdbCAContractInformationDescriptor, mstv.iisdbcacontractinformationdescriptor
ms.topic: interface
f1_keywords: 
 - "dvbsiparser/IIsdbCAContractInformationDescriptor"
req.header: dvbsiparser.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Dvbsiparser.idl
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
 - IIsdbCAContractInformationDescriptor
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IIsdbCAContractInformationDescriptor interface


## -description


Implements methods that get data from an Integrated Services Digital Broadcasting (ISDB) conditional access  (CA) contract information descriptor. The conditional access contract information  descriptor appears in the ISDB Service Information as part of the event information iable (EIT) or service description table (SDT). The <b>IIsdbaCAContractInformationDescriptor</b> Interface is used to check whether a program scheduled
for broadcast is a flator tiered-type service or event, or a pay-per-view event, and to check whether the program can be reserved for viewing or recording in advance. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IIsdbCAContractInformationDescriptor</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IIsdbCAContractInformationDescriptor</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IIsdbCAContractInformationDescriptor</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbcacontractinformationdescriptor-getcasystemid">GetCASystemId</a>
</td>
<td align="left" width="63%">
Gets the system identifier from a conditional access contract information descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbcacontractinformationdescriptor-getcaunitid">GetCAUnitId</a>
</td>
<td align="left" width="63%">
 Gets the identifier for a billing or nonbilling unit from a conditional access contract information descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbcacontractinformationdescriptor-getcontractverificationinfo">GetContractVerificationInfo</a>
</td>
<td align="left" width="63%">
 Gets contract verification data from  a conditional access contract information descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbcacontractinformationdescriptor-getcontractverificationinfolength">GetContractVerificationInfoLength</a>
</td>
<td align="left" width="63%">
 Gets the length of the contract verification information from a conditional access contract information descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbcacontractinformationdescriptor-getcountofrecords">GetCountOfRecords</a>
</td>
<td align="left" width="63%">
Gets the number of components in  a conditional access contract information descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbcacontractinformationdescriptor-getfeenamew">GetFeeNameW</a>
</td>
<td align="left" width="63%">
Gets the name of a fee from a conditional access contract information descriptor in Unicode-text format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbcacontractinformationdescriptor-getlength">GetLength</a>
</td>
<td align="left" width="63%">
 Gets the body length of a conditional access contract information descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbcacontractinformationdescriptor-getrecordcomponenttag">GetRecordComponentTag</a>
</td>
<td align="left" width="63%">
Gets the record component tag from a conditional access contract information descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbcacontractinformationdescriptor-gettag">GetTag</a>
</td>
<td align="left" width="63%">
Gets the tag that identifies a conditional access contract information descriptor.

</td>
</tr>
</table> 

