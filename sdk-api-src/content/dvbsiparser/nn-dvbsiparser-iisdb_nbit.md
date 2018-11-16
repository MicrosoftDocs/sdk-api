---
UID: NN:dvbsiparser.IISDB_NBIT
title: IISDB_NBIT
author: windows-sdk-content
description: Implements methods that get information from an Integrated Services Digital Broadcasting (ISDB) network broadcaster information table (NBIT). The NBIT describes the programs included in a multiplexed transport stream for an ISDB broadcast.
old-location: mstv\iisdb_nbit.htm
tech.root: mstv
ms.assetid: 32c15a03-6683-4b22-b374-a15784696368
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IISDB_NBIT, IISDB_NBIT interface [Microsoft TV Technologies], IISDB_NBIT interface [Microsoft TV Technologies],described, dvbsiparser/IISDB_NBIT, mstv.iisdb_nbit
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
 - IISDB_NBIT
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IISDB_NBIT interface


## -description


Implements methods that get information from an Integrated Services Digital Broadcasting (ISDB) network broadcaster information table (NBIT).
  The NBIT describes the programs included in a multiplexed transport stream for an ISDB broadcast.


To obtain a pointer to this interface, first make sure that the media graph is in a running state and that the stream you are tuned to contains an NBIT. Then:

<ol>
<li>Query the <a href="https://msdn.microsoft.com/22044a4c-480f-4c98-a78e-52c66a5eac99">BDA MPEG-2 Transport Information Filter</a> to obtain a pointer to the <a href="https://msdn.microsoft.com/6f07b4d2-7a52-448c-9e9f-729bd5261757">IPSITables</a> interface. (You can also go through the graph and query each filter until you find one that supports <b>IPSITables</b>.)</li>
<li>Call the <a href="https://msdn.microsoft.com/4b2362c7-bfcb-40b8-813d-1a904149600e">IPSITables::GetTable</a> method. The interface pointer for the desired table is returned in the <i>ppIUnknown</i> output parameter.
</li>
</ol>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IISDB_NBIT</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IISDB_NBIT</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IISDB_NBIT</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c747278a-dea7-4772-b37d-89c1deaaf91f">GetCountOfRecords</a>
</td>
<td align="left" width="63%">
Gets a value that specifies the number of records in the NBIT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/762b7d48-c74e-4d5a-9c99-890d613553fa">GetOriginalNetworkId</a>
</td>
<td align="left" width="63%">
Gets an identifier for the network that originated the broadcast.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2f4f5b5a-f03a-4b90-aa7c-2552841ba165">GetRecordCountOfDescriptors</a>
</td>
<td align="left" width="63%">
Gets the number of descriptors from the NBIT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bb022e1f-6f46-4cdc-8f43-4c4475acf621">GetRecordDescriptionBodyLocation</a>
</td>
<td align="left" width="63%">
Gets a value that indicates where the NBIT contents are described.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0f7da95d-ba3f-4cdc-aea0-38abae260159">GetRecordDescriptorByIndex</a>
</td>
<td align="left" width="63%">
Returns a descriptor for a specified record
  in an NBIT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/baec7c6a-67a7-4081-96ee-3cb35a72ff4e">GetRecordDescriptorByTag</a>
</td>
<td align="left" width="63%">
Gets a descriptor from a record in an NBIT
  by using the standard tag for the descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9535d587-3e37-4d12-9b96-66ff1c2cf6f3">GetRecordInformationId</a>
</td>
<td align="left" width="63%">
Gets a value that identifies the type of information in the NBIT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0f51abc1-d797-4666-b5d5-50560fd2f9f3">GetRecordInformationType</a>
</td>
<td align="left" width="63%">
Gets a value that identifies the type of information obtained from the NBIT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c8f58c17-b3b1-4fc8-b6e0-2ab23681280d">GetRecordKeys</a>
</td>
<td align="left" width="63%">
Gets the key IDs from the NBIT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3bfab381-f5af-4583-b268-72c83f3bfb8d">GetRecordMessageSectionNumber</a>
</td>
<td align="left" width="63%">
Gets a value that identifies a section within the NBIT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0ce49e6c-8a85-4620-a2ca-379c3bb30d64">GetRecordNumberOfKeys</a>
</td>
<td align="left" width="63%">
Gets the number of key IDs in the NBIT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/36786614-7b7e-4d76-9610-c969ad68f9d8">GetRecordUserDefined</a>
</td>
<td align="left" width="63%">
Gets a broadcaster-defined value from the NBIT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6de71e7e-7296-46ad-a0fa-3aadb9a24ab5">GetVersionHash</a>
</td>
<td align="left" width="63%">
Gets a hash value for this instance of an NBIT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1082700f-f52d-466e-8191-abbe0b5f8d66">GetVersionNumber</a>
</td>
<td align="left" width="63%">
Gets the version number from the NBIT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8c4e3f53-1b32-4374-915f-15651259dd55">Initialize</a>
</td>
<td align="left" width="63%">
Initializes an object that supports this interface.

</td>
</tr>
</table> 

