---
UID: NN:dvbsiparser.IISDB_BIT
title: IISDB_BIT
author: windows-driver-content
description: Implements methods that get information from an Integrated Services Digital Broadcasting (ISDB) broadcaster information table (BIT). A BIT contains a broadcaster unit and the service information transmission parameter for each broadcaster unit.
old-location: mstv\iisdb_bit.htm
old-project: mstv
ms.assetid: 0ec4497c-68c3-4b0e-a9e4-332e42b2c89b
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: IISDB_BIT, IISDB_BIT interface [Microsoft TV Technologies], IISDB_BIT interface [Microsoft TV Technologies], described, dvbsiparser/IISDB_BIT, mstv.iisdb_bit
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
req.typenames: DSROLE_UPGRADE_STATUS_INFO, *PDSROLE_UPGRADE_STATUS_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	dvbsiparser.h
api_name:
-	IISDB_BIT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IISDB_BIT interface


## -description



  Implements methods that get information from an Integrated Services Digital Broadcasting (ISDB) broadcaster information table (BIT). A BIT contains a broadcaster unit and the service information transmission parameter
  for each broadcaster unit.



To obtain a pointer to this interface, first make sure that the media graph is in a running state and that the stream you are tuned to contains an BIT. Then:

<ol>
<li>Query the <a href="https://msdn.microsoft.com/22044a4c-480f-4c98-a78e-52c66a5eac99">BDA MPEG-2 Transport Information Filter</a> to obtain a pointer to the <a href="https://msdn.microsoft.com/6f07b4d2-7a52-448c-9e9f-729bd5261757">IPSITables</a> interface. (You can also go through the graph and query each filter until you find one that supports <b>IPSITables</b>.)</li>
<li>Call the <a href="https://msdn.microsoft.com/4b2362c7-bfcb-40b8-813d-1a904149600e">IPSITables::GetTable</a> method. The interface pointer for the desired table is returned in the <i>ppIUnknown</i> output parameter.
</li>
</ol>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IISDB_BIT</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IISDB_BIT</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IISDB_BIT</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b0b38631-9b0c-4ebe-9cf5-6e5847261136">GetBroadcastViewPropriety</a>
</td>
<td align="left" width="63%">
Gets a flag that indicates whether the content is appropriate for an age-based category of viewer from the BIT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3f36c03a-462e-479a-ad8c-5322377dbca0">GetCountOfRecords</a>
</td>
<td align="left" width="63%">
Gets a value that specifies the number of records in the BIT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/69b1851b-b8a9-4dfe-be6b-ffadd2a83b12">GetCountOfTableDescriptors</a>
</td>
<td align="left" width="63%">
Gets the number of table descriptors in a BIT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/eb10f0a9-d673-46eb-bde1-3f22c518b05d">GetOriginalNetworkId</a>
</td>
<td align="left" width="63%">
Gets an identifier for the network that originated the broadcast.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9decce55-599b-42c2-a715-84a6f4eefc33">GetRecordBroadcasterId</a>
</td>
<td align="left" width="63%">
Gets a BIT record for a specific broadcaster.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/08df6f74-dbeb-4d32-8b0f-4ec88d35ff36">GetRecordCountOfDescriptors</a>
</td>
<td align="left" width="63%">
Gets the number of descriptors from the BIT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f3833ab6-39f8-499e-bd3f-f0f524a8b1d4">GetRecordDescriptorByIndex</a>
</td>
<td align="left" width="63%">
Returns a descriptor for a specified record
  in a BIT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9e22da6e-1721-46c5-9a98-7d21edaa6d14">GetRecordDescriptorByTag</a>
</td>
<td align="left" width="63%">
Gets a descriptor from a record in a BIT
  by using the standard tag for the descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5c6002b2-61c3-4d0c-87b9-682c3277792c">GetTableDescriptorByIndex</a>
</td>
<td align="left" width="63%">
Gets a descriptor for a specific BIT subtable.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ef54b6bc-7150-4246-8058-4e57f25c2ad3">GetTableDescriptorByTag</a>
</td>
<td align="left" width="63%">
Gets a descriptor from a subtable in a BIT
  by using the standard tag for the descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/26423a5f-710b-405f-acf2-1aafbeb304d2">GetVersionHash</a>
</td>
<td align="left" width="63%">
Gets a hash value for this instance of a BIT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/44f905e2-4814-4990-8a77-6ca6311c5505">GetVersionNumber</a>
</td>
<td align="left" width="63%">
Gets the version number from the BIT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff550945">Initialize</a>
</td>
<td align="left" width="63%">
Initializes an object that supports this interface.

</td>
</tr>
</table> 

