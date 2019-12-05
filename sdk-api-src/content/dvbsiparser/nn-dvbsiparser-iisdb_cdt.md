---
UID: NN:dvbsiparser.IISDB_CDT
title: IISDB_CDT (dvbsiparser.h)
description: Implements methods that get information from an Integrated Services Digital Broadcasting (ISDB) common data table (CDT). A CDT contains data, such as company logos, that is needed for receivers and stored in nonvolatile memory.
old-location: mstv\iisdb_cdt.htm
tech.root: mstv
ms.assetid: 6e0ceabb-4d67-46c1-9e7d-e00d5ad82280
ms.date: 12/05/2018
ms.keywords: IISDB_CDT, IISDB_CDT interface [Microsoft TV Technologies], IISDB_CDT interface [Microsoft TV Technologies],described, dvbsiparser/IISDB_CDT, mstv.iisdb_cdt
ms.topic: interface
f1_keywords:
- dvbsiparser/IISDB_CDT
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IISDB_CDT interface


## -description


Implements methods that get information from an Integrated Services Digital Broadcasting (ISDB)  common data table (CDT). A CDT contains data, such as company logos, that is needed for receivers and stored in
  nonvolatile memory.


To obtain a pointer to this interface, first make sure that the media graph is in a running state and that the stream you are tuned to contains a CDT. Then:

<ol>
<li>Query the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/bda-mpeg-2-transport-information-filter">BDA MPEG-2 Transport Information Filter</a> to obtain a pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/mpeg2psiparser/nn-mpeg2psiparser-ipsitables">IPSITables</a> interface. (You can also go through the graph and query each filter until you find one that supports <b>IPSITables</b>.)</li>
<li>Call the <a href="https://docs.microsoft.com/windows/desktop/api/mpeg2psiparser/nf-mpeg2psiparser-ipsitables-gettable">IPSITables::GetTable</a> method. The interface pointer for the desired table is returned in the <i>ppIUnknown</i> output parameter.
</li>
</ol>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IISDB_CDT</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IISDB_CDT</b> also has these types of members:
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
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdb_cdt-getcountoftabledescriptors">GetCountOfTableDescriptors</a>
</td>
<td align="left" width="63%">
Gets the number of logo descriptors from the CDT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdb_cdt-getdatamodule">GetDataModule</a>
</td>
<td align="left" width="63%">
Gets data from the data module in a CDT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdb_cdt-getdatatype">GetDataType</a>
</td>
<td align="left" width="63%">
Gets the data type from the CDT. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdb_cdt-getdownloaddataid">GetDownloadDataId</a>
</td>
<td align="left" width="63%">
Gets an identifier for the data to be downloaded.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdb_cdt-getoriginalnetworkid">GetOriginalNetworkId</a>
</td>
<td align="left" width="63%">
Gets an identifier for the network that originated the broadcast.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdb_cdt-getsectionnumber">GetSectionNumber</a>
</td>
<td align="left" width="63%">
Gets a value indicating the ordinal position of a subtable within the CDT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdb_cdt-getsizeofdatamodule">GetSizeOfDataModule</a>
</td>
<td align="left" width="63%">
Gets the size, in bytes, of the data module from a CDT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/dd694308(v=vs.85)">GetTableDescriptorByIndex</a>
</td>
<td align="left" width="63%">
Returns a descriptor for a specified subtable
  in a CDT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdb_cdt-gettabledescriptorbytag">GetTableDescriptorByTag</a>
</td>
<td align="left" width="63%">
Gets a descriptor from a subtable in a CDT
  by using the standard tag for the descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdb_cdt-getversionhash">GetVersionHash</a>
</td>
<td align="left" width="63%">
Gets a hash value for this instance of a CDT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdb_cdt-getversionnumber">GetVersionNumber</a>
</td>
<td align="left" width="63%">
Gets the version number from the CDT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdb_cdt-initialize">Initialize</a>
</td>
<td align="left" width="63%">
Initializes an object that implements this interface.

</td>
</tr>
</table> 

