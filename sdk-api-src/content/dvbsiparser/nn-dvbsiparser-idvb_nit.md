---
UID: NN:dvbsiparser.IDVB_NIT
title: IDVB_NIT (dvbsiparser.h)
author: windows-sdk-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
old-location: mstv\idvb_nit.htm
tech.root: mstv
ms.assetid: 70b638ae-0152-4a44-aeb1-f3ac382c19ce
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDVB_NIT, IDVB_NIT interface [Microsoft TV Technologies], IDVB_NIT interface [Microsoft TV Technologies],described, IDVB_NITInterface, dvbsiparser/IDVB_NIT, mstv.idvb_nit
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
 - IDVB_NIT
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDVB_NIT interface


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        

The <b>IDVB_NIT</b> interface enables the client to get information from a network information table (NIT). The <a href="https://msdn.microsoft.com/a7c802ad-908f-4778-b8db-02fff4f3a13e">IDvbSiParser::GetNIT</a> method returns a pointer to this interface.

A NIT contains information about the network and the physical organization of the transport streams. Because a network typically carries more than one transport stream, the NIT can provide information for tuning and for locating particular transport streams. A NIT carried on one network may contain information about another network.

The original_network_id and transport_stream_id fields together uniquely define a transport stream within the network.

The NIT may contain one or more table-wide descriptors. In addition, each record in the NIT may have one or more descriptors. To get the table-wide descriptors, use the <b>GetTableDescriptorByIndex</b> or <b>GetTableDescriptorByTag</b> method. To get the record descriptors, use the <b>GetRecordDescriptorByIndex</b> or <b>GetRecordDescriptorByTag</b> method.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDVB_NIT</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDVB_NIT</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDVB_NIT</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/068f5dd8-f0fc-4d34-a49c-91cedb7bf7e7">ConvertNextToCurrent</a>
</td>
<td align="left" width="63%">
Converts a <i>next</i> table to a <i>current</i> table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fb0f8071-575a-4bbd-b34b-b8d92c17c476">GetCountOfRecords</a>
</td>
<td align="left" width="63%">
Returns the number of records in the NIT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ec87b75b-3eae-4227-bbd5-0c5df24aa985">GetCountOfTableDescriptors</a>
</td>
<td align="left" width="63%">
Returns the number of table-wide descriptors in the NIT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/86841b62-d6c0-4911-baf7-dd6d1a08a770">GetNetworkId</a>
</td>
<td align="left" width="63%">
Returns the network identifier for the NIT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6073ab66-7011-4983-a11e-1c26a3549423">GetNextTable</a>
</td>
<td align="left" width="63%">
Retrieves the next table that follows the current table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3f3e43d8-5063-4fac-bbec-22b6876716f0">GetRecordCountOfDescriptors</a>
</td>
<td align="left" width="63%">
Returns the number of descriptors for a record in the NIT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b81651b1-2b70-4012-b219-57d495724033">GetRecordDescriptorByIndex</a>
</td>
<td align="left" width="63%">
Retrieves a descriptor for a specified record in the NIT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e4d3da3c-3631-41c2-b463-a90cd54e42f9">GetRecordDescriptorByTag</a>
</td>
<td align="left" width="63%">
Searches a record in the NIT for a descriptor with a specified descriptor tag.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3179be9a-de2d-4cb3-ace2-ad5af66d35c8">GetRecordOriginalNetworkId</a>
</td>
<td align="left" width="63%">
Returns the original network identifier for a record in the NIT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ed2b9fcc-fd7d-4477-9ff5-cbb7912eac26">GetRecordTransportStreamId</a>
</td>
<td align="left" width="63%">
Returns the transport stream identifier (TSID) for a record in the NIT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fa9d16c3-da30-44ab-9c40-7bc24b54eaaf">GetTableDescriptorByIndex</a>
</td>
<td align="left" width="63%">
Retrieves a table-wide descriptor for the NIT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/94182dbb-d96c-45e9-953c-faf8e0403aac">GetTableDescriptorByTag</a>
</td>
<td align="left" width="63%">
Searches the NIT for a table-wide descriptor with the specified descriptor tag.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b12a2363-a8a6-49b4-8d12-1e947d659eee">GetVersionHash</a>
</td>
<td align="left" width="63%">
Returns a hash value for this table instance.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/75f7dc3b-8631-4a33-90f2-ace95e4112a7">GetVersionNumber</a>
</td>
<td align="left" width="63%">
Returns the version number for the NIT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7f59b8d4-520c-441d-bbd3-60ab8962e3b4">Initialize</a>
</td>
<td align="left" width="63%">
Initializes the object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f299cdcb-d0da-4e79-9f2d-c792bbb43313">RegisterForNextTable</a>
</td>
<td align="left" width="63%">
Registers the client to be notified when a <i>next</i> table arrives that will replace the current table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b5405814-1e7c-470f-a8bc-d16d16bdb526">RegisterForWhenCurrent</a>
</td>
<td align="left" width="63%">
Registers the client to be notified when the table becomes current.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/07d18f73-e852-4c88-a2e2-e8f4198ca799">BDA Interfaces</a>
 

 

