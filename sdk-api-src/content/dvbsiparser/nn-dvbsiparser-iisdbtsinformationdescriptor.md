---
UID: NN:dvbsiparser.IIsdbTSInformationDescriptor
title: IIsdbTSInformationDescriptor (dvbsiparser.h)
author: windows-sdk-content
description: Implements methods that get data from an Integrated Services Digital Broadcasting (ISDB) transport stream (TS) information descriptor.
old-location: mstv\iisdbtsinformationdescriptor.htm
tech.root: mstv
ms.assetid: 3c8cd33c-5c2a-48a4-9e8a-f7dd03560848
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IIsdbTSInformationDescriptor, IIsdbTSInformationDescriptor interface [Microsoft TV Technologies], IIsdbTSInformationDescriptor interface [Microsoft TV Technologies],described, dvbsiparser/IIsdbTSInformationDescriptor, mstv.iisdbtsinformationdescriptor
ms.topic: interface
f1_keywords: 
 - "dvbsiparser/IIsdbTSInformationDescriptor"
dev_langs:
 - c++
req.header: dvbsiparser.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - IIsdbTSInformationDescriptor
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IIsdbTSInformationDescriptor interface


## -description


Implements methods that get data from an Integrated Services Digital Broadcasting (ISDB) transport stream (TS) information descriptor. The TS information descriptor appears in the ISDB Service Information as part of the event information table (EIT). This descriptor specifies the remote control key identifier assigned to the applicable
transport stream. It indicates the relationship between the service identifier and the transmission layer during
hierarchical transmission.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IIsdbTSInformationDescriptor</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IIsdbTSInformationDescriptor</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IIsdbTSInformationDescriptor</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbtsinformationdescriptor-getcountofrecords">GetCountOfRecords</a>
</td>
<td align="left" width="63%">
 Gets the number of records in an ISDB TS information descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbtsinformationdescriptor-getlength">GetLength</a>
</td>
<td align="left" width="63%">
 Gets the body length of an ISDB TS information descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbtsinformationdescriptor-getrecordnumberofservices">GetRecordNumberOfServices</a>
</td>
<td align="left" width="63%">
Gets the number of service records in an ISDB TS information descriptor. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/dd694281(v=vs.85)">GetRecordServiceIdByIndex</a>
</td>
<td align="left" width="63%">
 Gets a service identifier from a specified service record in an ISDB TS information descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbtsinformationdescriptor-getrecordtransmissiontypeinfo">GetRecordTransmissionTypeInfo</a>
</td>
<td align="left" width="63%">
 Gets the transmission type from an ISDB TS information descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbtsinformationdescriptor-getremotecontrolkeyid">GetRemoteControlKeyId</a>
</td>
<td align="left" width="63%">
 Gets the remote control key ID from an ISDB TS information descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbtsinformationdescriptor-gettag">GetTag</a>
</td>
<td align="left" width="63%">
Gets the tag that identifies an ISDB TS information descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbtsinformationdescriptor-gettsnamew">GetTSNameW</a>
</td>
<td align="left" width="63%">
 Gets the transport stream name from  an ISDB TS information descriptor, in Unicode text format.

</td>
</tr>
</table> 

