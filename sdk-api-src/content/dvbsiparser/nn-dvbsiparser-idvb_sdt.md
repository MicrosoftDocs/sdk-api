---
UID: NN:dvbsiparser.IDVB_SDT
title: IDVB_SDT (dvbsiparser.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
old-location: mstv\idvb_sdt.htm
tech.root: mstv
ms.assetid: bb473a7e-8957-4e85-98d0-13c6992fbf37
ms.date: 12/05/2018
ms.keywords: IDVB_SDT, IDVB_SDT interface [Microsoft TV Technologies], IDVB_SDT interface [Microsoft TV Technologies],described, IDVB_SDTInterface, dvbsiparser/IDVB_SDT, mstv.idvb_sdt
f1_keywords:
- dvbsiparser/IDVB_SDT
dev_langs:
- c++
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
- IDVB_SDT
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDVB_SDT interface


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        

The <b>IDVB_SDT</b> interface enables the client to get information from a service description table (SDT). The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbsiparser-getsdt">IDvbSiParser::GetSDT</a> method returns a pointer to this interface.

An SDT describes one or more services that are carried in a particular transport stream. The services may be carried in the same transport stream that carries the SDT, or a different transport stream.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDVB_SDT</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDVB_SDT</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDVB_SDT</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvb_sdt-convertnexttocurrent">ConvertNextToCurrent</a>
</td>
<td align="left" width="63%">
Converts a <i>next</i> table to a <i>current</i> table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvb_sdt-getcountofrecords">GetCountOfRecords</a>
</td>
<td align="left" width="63%">
Returns the number of records in the SDT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvb_sdt-getnexttable">GetNextTable</a>
</td>
<td align="left" width="63%">
Retrieves the <i>next</i> table that follows the current table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvb_sdt-getoriginalnetworkid">GetOriginalNetworkId</a>
</td>
<td align="left" width="63%">
Returns the original network identifier.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvb_sdt-getrecordcountofdescriptors">GetRecordCountOfDescriptors</a>
</td>
<td align="left" width="63%">
Returns the number of descriptors for a record in the SDT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvb_sdt-getrecorddescriptorbyindex">GetRecordDescriptorByIndex</a>
</td>
<td align="left" width="63%">
Retrieves a descriptor for a specified record in the SDT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvb_sdt-getrecorddescriptorbytag">GetRecordDescriptorByTag</a>
</td>
<td align="left" width="63%">
Searches a record in the SDT for a descriptor with a specified descriptor tag.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvb_sdt-getrecordeitpresentfollowingflag">GetRecordEITPresentFollowingFlag</a>
</td>
<td align="left" width="63%">
Queries whether the current transport stream contains present/following EIT information for a particular service.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvb_sdt-getrecordeitscheduleflag">GetRecordEITScheduleFlag</a>
</td>
<td align="left" width="63%">
Queries whether the current transport stream contains schedule EIT information for a particular service.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvb_sdt-getrecordfreecamode">GetRecordFreeCAMode</a>
</td>
<td align="left" width="63%">
Queries whether any of the component streams for a particular service are scrambled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvb_sdt-getrecordrunningstatus">GetRecordRunningStatus</a>
</td>
<td align="left" width="63%">
Returns the running status of a particular service in the SDT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvb_sdt-getrecordserviceid">GetRecordServiceId</a>
</td>
<td align="left" width="63%">
Returns the service identifier for a record in the SDT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvb_sdt-gettransportstreamid">GetTransportStreamId</a>
</td>
<td align="left" width="63%">
Returns the transport stream identifier (TSID) for the SDT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvb_sdt-getversionhash">GetVersionHash</a>
</td>
<td align="left" width="63%">
Returns a hash value for this table instance.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvb_sdt-getversionnumber">GetVersionNumber</a>
</td>
<td align="left" width="63%">
Returns the version number for the SDT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvb_sdt-initialize">Initialize</a>
</td>
<td align="left" width="63%">
Initializes the object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvb_sdt-registerfornexttable">RegisterForNextTable</a>
</td>
<td align="left" width="63%">
Registers the client to be notified when a <i>next</i> table arrives that will replace the current table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvb_sdt-registerforwhencurrent">RegisterForWhenCurrent</a>
</td>
<td align="left" width="63%">
Registers the client to be notified when the table becomes current.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/bda-interfaces">BDA Interfaces</a>
 

 

