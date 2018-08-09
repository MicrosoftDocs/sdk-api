---
UID: NN:dvbsiparser.IDvbLogicalChannelDescriptor
title: IDvbLogicalChannelDescriptor
author: windows-sdk-content
description: The IDvbLogicalChannelDescriptor interface enables the client to get a logical channel descriptor from a DVB stream.
old-location: mstv\idvblogicalchanneldescriptor.htm
old-project: mstv
ms.assetid: 6e0a99e9-088f-420c-bb60-2d324aa28227
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IDvbLogicalChannelDescriptor, IDvbLogicalChannelDescriptor interface [DirectShow], IDvbLogicalChannelDescriptor interface [DirectShow],described, IDvbLogicalChannelDescriptorInterface, dvbsiparser/IDvbLogicalChannelDescriptor, mstv.idvblogicalchanneldescriptor
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
 - IDvbLogicalChannelDescriptor
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDvbLogicalChannelDescriptor interface


## -description



<div class="alert"><b>Note</b>  This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        </div>
<div> </div>


The <b>IDvbLogicalChannelDescriptor</b> interface enables the client to get a logical channel descriptor from a DVB stream. The logical channel descriptor may be present in the network information table (NIT).


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDvbLogicalChannelDescriptor</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDvbLogicalChannelDescriptor</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDvbLogicalChannelDescriptor</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/97cadf6c-2549-4a7f-9ecb-c16298769a21">GetCountOfRecords</a>
</td>
<td align="left" width="63%">
Returns the number of records in the logical channel descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/20c0f2a8-e4f5-4516-8c19-30cd19f0816e">GetLength</a>
</td>
<td align="left" width="63%">
Returns the length of the descriptor body.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fa74587a-ba11-449c-ba0d-bea371e7f019">GetRecordLogicalChannelNumber</a>
</td>
<td align="left" width="63%">
Returns the logical channel number at a specified index in the channel list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ab0670e9-400c-4a3f-8afa-e323a3915dc3">GetRecordServiceId</a>
</td>
<td align="left" width="63%">
Returns the service identifier at a specified index in the channel list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fce4b74e-e7bb-419d-bd5a-849c2d050ee9">GetTag</a>
</td>
<td align="left" width="63%">
Returns the descriptor tag.

</td>
</tr>
</table> 


## -remarks



To obtain a pointer to this interface, do the following:

<ol>
<li>Call <a href="https://msdn.microsoft.com/a7c802ad-908f-4778-b8db-02fff4f3a13e">IDvbSiParser::GetNIT</a> to get the <a href="https://msdn.microsoft.com/70b638ae-0152-4a44-aeb1-f3ac382c19ce">IDVB_NIT</a> interface.</li>
<li>Call <a href="https://msdn.microsoft.com/e4d3da3c-3631-41c2-b463-a90cd54e42f9">IDVB_NIT::GetRecordDescriptorByTag</a> and pass in the logical channel descriptor tag (0x83). If the descriptor is present, the method returns an <a href="https://msdn.microsoft.com/efca0ecf-eb3e-4dcd-a674-b8fe1a66ff84">IGenericDescriptor</a> pointer.</li>
<li>Query the returned <a href="https://msdn.microsoft.com/efca0ecf-eb3e-4dcd-a674-b8fe1a66ff84">IGenericDescriptor</a> pointer for the <b>IDvbLogicalChannelDescriptor</b> interface.</li>
</ol>



## -see-also




<a href="https://msdn.microsoft.com/07d18f73-e852-4c88-a2e2-e8f4198ca799">BDA Interfaces</a>
 

 

