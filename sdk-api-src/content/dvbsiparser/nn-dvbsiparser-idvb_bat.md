---
UID: NN:dvbsiparser.IDVB_BAT
title: IDVB_BAT
author: windows-sdk-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
old-location: mstv\idvb_bat.htm
tech.root: mstv
ms.assetid: c312a152-21ee-4708-90a8-ab9bde9a2011
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IDVB_BAT, IDVB_BAT interface [Microsoft TV Technologies], IDVB_BAT interface [Microsoft TV Technologies],described, IDVB_BATInterface, dvbsiparser/IDVB_BAT, mstv.idvb_bat
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IDVB_BAT
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDVB_BAT interface


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        

The <b>IDVB_BAT</b> interface enables the client to get data from a bouquet association table (BAT). The <a href="https://msdn.microsoft.com/dc9cd50f-a9cc-436c-a416-9fc4de506a9e">IDvbSiParser::GetBAT</a> method returns a pointer to this interface.

A bouquet is a collection of services that are marketed as one entity. A single bouquet may contain several transport streams that are delivered across different distribution media (satellite, cable, or terrestrial).

The BAT may contain one or more table-wide descriptors. In addition, each record in the BAT may have one or more descriptors. To get the table-wide descriptors, use the <b>GetTableDescriptorByIndex</b> or <b>GetTableDescriptorByTag</b> method. To get the record descriptors, use the <b>GetRecordDescriptorByIndex</b> or <b>GetRecordDescriptorByTag</b> method.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDVB_BAT</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDVB_BAT</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDVB_BAT</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/befcd47c-e05e-4a75-a588-bebdb1cc3218">ConvertNextToCurrent</a>
</td>
<td align="left" width="63%">
Converts a <i>next</i> table to a <i>current</i> table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/43c8d96d-24a7-459b-8221-daef7759c603">GetBouquetId</a>
</td>
<td align="left" width="63%">
Returns the bouquet identifier for the BAT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/feb31eca-d746-48cf-8c1b-06dd7816725b">GetCountOfRecords</a>
</td>
<td align="left" width="63%">
Returns the number of records in the BAT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8f373cbe-9d07-41c2-83a5-c25bc66f6263">GetCountOfTableDescriptors</a>
</td>
<td align="left" width="63%">
Returns the number of table-wide descriptors in the BAT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9ba93496-d32f-44f1-83d8-1cfb61b689e9">GetNextTable</a>
</td>
<td align="left" width="63%">
Retrieves the <i>next</i> table that follows the current table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d3ef02f2-a593-4439-a460-e2b5fcd0ef70">GetRecordCountOfDescriptors</a>
</td>
<td align="left" width="63%">
Returns the number of descriptors for a record in the BAT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ea1ace90-4378-4dec-9326-70e6f9814dde">GetRecordDescriptorByIndex</a>
</td>
<td align="left" width="63%">
Retrieves a descriptor for a specified record in the BAT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/48818e59-6bf0-4f54-8b53-e61fa8b349b3">GetRecordDescriptorByTag</a>
</td>
<td align="left" width="63%">
Searches a record in the BAT for a descriptor with a specified descriptor tag.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b59aaea4-4960-4c82-b949-e8372c1e3f4c">GetRecordOriginalNetworkId</a>
</td>
<td align="left" width="63%">
Returns the original network identifier for a record in the BAT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fdb406d1-5242-4f3e-a1c9-b10296d98d67">GetRecordTransportStreamId</a>
</td>
<td align="left" width="63%">
Returns the transport stream identifier (TSID) for a record in the BAT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fa985aea-3822-439e-9a83-916cc1c9ae93">GetTableDescriptorByIndex</a>
</td>
<td align="left" width="63%">
Retrieves a table-wide descriptor for the BAT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9c989b8d-0cd0-4556-bc96-a464b95911d0">GetTableDescriptorByTag</a>
</td>
<td align="left" width="63%">
Searches the BAT for a table-wide descriptor with the specified descriptor tag.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2548a4b5-7789-42ef-9094-22deb6d72260">GetVersionNumber</a>
</td>
<td align="left" width="63%">
Returns the version number for the BAT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/76c0eabe-b2af-44ed-9afb-9b97e7e8c5df">Initialize</a>
</td>
<td align="left" width="63%">
Initializes the object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/77c2d270-72ab-4ae6-84dd-c28c231094ad">RegisterForNextTable</a>
</td>
<td align="left" width="63%">
Registers the client to be notified when a <i>next</i> table arrives that will replace the current table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d68cd8f7-e152-4105-8bc3-e9dad68e4e68">RegisterForWhenCurrent</a>
</td>
<td align="left" width="63%">
Registers the client to be notified when the table becomes current.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/07d18f73-e852-4c88-a2e2-e8f4198ca799">BDA Interfaces</a>
 

 

