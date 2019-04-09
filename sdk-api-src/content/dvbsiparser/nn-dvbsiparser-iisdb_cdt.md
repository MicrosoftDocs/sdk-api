---
UID: NN:dvbsiparser.IISDB_CDT
title: IISDB_CDT (dvbsiparser.h)
author: windows-sdk-content
description: Implements methods that get information from an Integrated Services Digital Broadcasting (ISDB) common data table (CDT). A CDT contains data, such as company logos, that is needed for receivers and stored in nonvolatile memory.
old-location: mstv\iisdb_cdt.htm
tech.root: mstv
ms.assetid: 6e0ceabb-4d67-46c1-9e7d-e00d5ad82280
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IISDB_CDT, IISDB_CDT interface [Microsoft TV Technologies], IISDB_CDT interface [Microsoft TV Technologies],described, dvbsiparser/IISDB_CDT, mstv.iisdb_cdt
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
 - IISDB_CDT
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IISDB_CDT interface


## -description


Implements methods that get information from an Integrated Services Digital Broadcasting (ISDB)  common data table (CDT). A CDT contains data, such as company logos, that is needed for receivers and stored in
  nonvolatile memory.


To obtain a pointer to this interface, first make sure that the media graph is in a running state and that the stream you are tuned to contains a CDT. Then:

<ol>
<li>Query the <a href="https://msdn.microsoft.com/22044a4c-480f-4c98-a78e-52c66a5eac99">BDA MPEG-2 Transport Information Filter</a> to obtain a pointer to the <a href="https://msdn.microsoft.com/en-us/library/Dd694840(v=VS.85).aspx">IPSITables</a> interface. (You can also go through the graph and query each filter until you find one that supports <b>IPSITables</b>.)</li>
<li>Call the <a href="https://msdn.microsoft.com/en-us/library/Dd694841(v=VS.85).aspx">IPSITables::GetTable</a> method. The interface pointer for the desired table is returned in the <i>ppIUnknown</i> output parameter.
</li>
</ol>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IISDB_CDT</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IISDB_CDT</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IISDB_CDT</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ea01a53f-8d0b-4594-87b4-d293901fca19">GetCountOfTableDescriptors</a>
</td>
<td align="left" width="63%">
Gets the number of logo descriptors from the CDT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b7ff7e8a-17bd-46aa-bf9b-74f3e33a7ce2">GetDataModule</a>
</td>
<td align="left" width="63%">
Gets data from the data module in a CDT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/843e1a0a-b4bb-487e-aa21-1bd6c32cceae">GetDataType</a>
</td>
<td align="left" width="63%">
Gets the data type from the CDT. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/87cd757e-ed10-4ad2-a9d5-4a92b8d48cd2">GetDownloadDataId</a>
</td>
<td align="left" width="63%">
Gets an identifier for the data to be downloaded.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/67adf536-1163-45e3-893c-e9501fefafe7">GetOriginalNetworkId</a>
</td>
<td align="left" width="63%">
Gets an identifier for the network that originated the broadcast.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/61825be5-01c4-4d5f-be4a-6752ebf8dee8">GetSectionNumber</a>
</td>
<td align="left" width="63%">
Gets a value indicating the ordinal position of a subtable within the CDT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c05a8c14-f0da-49d7-be34-1cac435a98da">GetSizeOfDataModule</a>
</td>
<td align="left" width="63%">
Gets the size, in bytes, of the data module from a CDT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e345e860-247a-4c30-876b-c0e6c82767b8">GetTableDescriptorByIndex</a>
</td>
<td align="left" width="63%">
Returns a descriptor for a specified subtable
  in a CDT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c06f9d03-a46a-4c3f-bacc-a78f79c411c3">GetTableDescriptorByTag</a>
</td>
<td align="left" width="63%">
Gets a descriptor from a subtable in a CDT
  by using the standard tag for the descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b6c3dd34-8db5-45a4-9c13-7e05d94c58b7">GetVersionHash</a>
</td>
<td align="left" width="63%">
Gets a hash value for this instance of a CDT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4c88ecdb-8e01-4fec-96f2-c67331b6d071">GetVersionNumber</a>
</td>
<td align="left" width="63%">
Gets the version number from the CDT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0430d839-4b7f-4d1c-9e5b-bd794d67f065">Initialize</a>
</td>
<td align="left" width="63%">
Initializes an object that implements this interface.

</td>
</tr>
</table> 

