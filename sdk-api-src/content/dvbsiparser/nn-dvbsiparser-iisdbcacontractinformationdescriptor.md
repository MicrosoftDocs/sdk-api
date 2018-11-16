---
UID: NN:dvbsiparser.IIsdbCAContractInformationDescriptor
title: IIsdbCAContractInformationDescriptor
author: windows-sdk-content
description: Implements methods that get data from an Integrated Services Digital Broadcasting (ISDB) conditional access (CA) contract information descriptor.
old-location: mstv\iisdbcacontractinformationdescriptor.htm
tech.root: mstv
ms.assetid: d877a625-d683-4472-98de-f24c165c753a
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IIsdbCAContractInformationDescriptor, IIsdbCAContractInformationDescriptor interface [Microsoft TV Technologies], IIsdbCAContractInformationDescriptor interface [Microsoft TV Technologies],described, dvbsiparser/IIsdbCAContractInformationDescriptor, mstv.iisdbcacontractinformationdescriptor
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IIsdbCAContractInformationDescriptor interface


## -description


Implements methods that get data from an Integrated Services Digital Broadcasting (ISDB) conditional access  (CA) contract information descriptor. The conditional access contract information  descriptor appears in the ISDB Service Information as part of the event information iable (EIT) or service description table (SDT). The <b>IIsdbaCAContractInformationDescriptor</b> Interface is used to check whether a program scheduled
for broadcast is a flator tiered-type service or event, or a pay-per-view event, and to check whether the program can be reserved for viewing or recording in advance. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IIsdbCAContractInformationDescriptor</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IIsdbCAContractInformationDescriptor</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/cb9f55c1-7967-43e4-9cb3-1d7cdf20c70a">GetCASystemId</a>
</td>
<td align="left" width="63%">
Gets the system identifier from a conditional access contract information descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1e50f417-6403-499a-944c-2926a18dada1">GetCAUnitId</a>
</td>
<td align="left" width="63%">
 Gets the identifier for a billing or nonbilling unit from a conditional access contract information descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bfec246a-df34-46c3-9529-dc1fa75582da">GetContractVerificationInfo</a>
</td>
<td align="left" width="63%">
 Gets contract verification data from  a conditional access contract information descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a7000edd-72a1-4979-b603-a42eecc691d7">GetContractVerificationInfoLength</a>
</td>
<td align="left" width="63%">
 Gets the length of the contract verification information from a conditional access contract information descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/00df3bb9-494b-4e2c-b836-4893fd6eff8c">GetCountOfRecords</a>
</td>
<td align="left" width="63%">
Gets the number of components in  a conditional access contract information descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c2fcdcc1-acca-417e-bcf5-baad4ea07cef">GetFeeNameW</a>
</td>
<td align="left" width="63%">
Gets the name of a fee from a conditional access contract information descriptor in Unicode-text format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f8a4f327-c3ad-4170-91c8-57f6dc22e162">GetLength</a>
</td>
<td align="left" width="63%">
 Gets the body length of a conditional access contract information descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cd032a24-228a-47e3-97f4-1046b426c587">GetRecordComponentTag</a>
</td>
<td align="left" width="63%">
Gets the record component tag from a conditional access contract information descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f64110eb-1f96-421c-8f32-3d82a5ed4378">GetTag</a>
</td>
<td align="left" width="63%">
Gets the tag that identifies a conditional access contract information descriptor.

</td>
</tr>
</table> 

