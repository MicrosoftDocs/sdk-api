---
UID: NN:dvbsiparser.IDvbServiceDescriptor
title: IDvbServiceDescriptor
author: windows-sdk-content
description: Implements methods that get data from a Digital Video Broadcast (DVB) service descriptor.
old-location: mstv\idvbservicedescriptor.htm
old-project: mstv
ms.assetid: 7024259f-3dcf-46e0-9984-d5924c9e5b54
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: IDvbServiceDescriptor, IDvbServiceDescriptor interface [Microsoft TV Technologies], IDvbServiceDescriptor interface [Microsoft TV Technologies],described, dvbsiparser/IDvbServiceDescriptor, mstv.idvbservicedescriptor
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
tech.root: 
req.typenames: DSROLE_UPGRADE_STATUS_INFO, *PDSROLE_UPGRADE_STATUS_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dvbsiparser.h
api_name:
 - IDvbServiceDescriptor
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDvbServiceDescriptor interface


## -description


Implements methods that get data from a Digital Video Broadcast (DVB) service descriptor.  The service  descriptor  appears in the DVB service information as part of the  service description table (SDT) or selection information table (SIT). It describes the service type and provides the names of the service provider and the service in text form.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDvbServiceDescriptor</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDvbServiceDescriptor</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/e8c35777-0a54-4b26-b5a2-629ba3cb3928">GetLength</a>
</td>
<td align="left" width="63%">
Gets the body length from a DVB service descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c0441e70-270e-4685-9107-865c2b6398e9">GetProcessedServiceName</a>
</td>
<td align="left" width="63%">
Gets the processed service name from a DVB service descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d3c59ebc-fc32-49ba-86b3-5737c3af2225">GetServiceName</a>
</td>
<td align="left" width="63%">
Gets the service name from a DVB service descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/232bdf11-b9f5-48cd-8cd5-f03cd589d43e">GetServiceNameEmphasized</a>
</td>
<td align="left" width="63%">
Gets the emphasized service name from a DVB service descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ea5d358f-7da3-47c4-9172-7e5c60a61f84">GetServiceProviderName</a>
</td>
<td align="left" width="63%">
Gets the service provider name from a DVB service descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e4c6f1f1-8cf8-4848-bb88-e1d11f4fe045">GetServiceProviderNameW</a>
</td>
<td align="left" width="63%">
Gets the service provider name string from a DVB service descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f13b6b0e-d4bb-42a6-9bab-dc3e13bc26e9">GetServiceType</a>
</td>
<td align="left" width="63%">
Gets the service type from a DVB service descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0cdf6279-3156-43eb-97e3-58a4f9d93cc6">GetTag</a>
</td>
<td align="left" width="63%">
Gets the identifying tag from a DVB service descriptor.

</td>
</tr>
</table> 

