---
UID: NN:dvbsiparser.IIsdbTSInformationDescriptor
title: IIsdbTSInformationDescriptor
author: windows-sdk-content
description: Implements methods that get data from an Integrated Services Digital Broadcasting (ISDB) transport stream (TS) information descriptor.
old-location: mstv\iisdbtsinformationdescriptor.htm
tech.root: mstv
ms.assetid: 3c8cd33c-5c2a-48a4-9e8a-f7dd03560848
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IIsdbTSInformationDescriptor, IIsdbTSInformationDescriptor interface [Microsoft TV Technologies], IIsdbTSInformationDescriptor interface [Microsoft TV Technologies],described, dvbsiparser/IIsdbTSInformationDescriptor, mstv.iisdbtsinformationdescriptor
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IIsdbTSInformationDescriptor interface


## -description


Implements methods that get data from an Integrated Services Digital Broadcasting (ISDB) transport stream (TS) information descriptor. The TS information descriptor appears in the ISDB Service Information as part of the event information table (EIT). This descriptor specifies the remote control key identifier assigned to the applicable
transport stream. It indicates the relationship between the service identifier and the transmission layer during
hierarchical transmission.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IIsdbTSInformationDescriptor</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IIsdbTSInformationDescriptor</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/97e0d307-f41d-44e3-8f42-d00fecbcd61e">GetCountOfRecords</a>
</td>
<td align="left" width="63%">
 Gets the number of records in an ISDB TS information descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/17c74b77-0754-47de-97f8-db1c15707276">GetLength</a>
</td>
<td align="left" width="63%">
 Gets the body length of an ISDB TS information descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bf9ec856-951e-4a75-a136-9fa6eaf9e8cd">GetRecordNumberOfServices</a>
</td>
<td align="left" width="63%">
Gets the number of service records in an ISDB TS information descriptor. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/40738938-226d-4220-8092-a029bd6c038d">GetRecordServiceIdByIndex</a>
</td>
<td align="left" width="63%">
 Gets a service identifier from a specified service record in an ISDB TS information descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/992ef7de-ccf8-42a1-bb83-4b5f396164ce">GetRecordTransmissionTypeInfo</a>
</td>
<td align="left" width="63%">
 Gets the transmission type from an ISDB TS information descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/51162c5e-9ece-4c3d-9ab1-03d03a326efe">GetRemoteControlKeyId</a>
</td>
<td align="left" width="63%">
 Gets the remote control key ID from an ISDB TS information descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/77a7b225-2e7e-4fa2-a8f0-a5f18850cde6">GetTag</a>
</td>
<td align="left" width="63%">
Gets the tag that identifies an ISDB TS information descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4c8900d1-1047-4b11-87e0-da1a72f511f7">GetTSNameW</a>
</td>
<td align="left" width="63%">
 Gets the transport stream name from  an ISDB TS information descriptor, in Unicode text format.

</td>
</tr>
</table> 

