---
UID: NN:dvbsiparser.IIsdbComponentGroupDescriptor
title: IIsdbComponentGroupDescriptor (dvbsiparser.h)
description: Implements methods that get data from an Integrated Services Digital Broadcasting (ISDB) component group descriptor.
old-location: mstv\iisdbcomponentgroupdescriptor.htm
tech.root: mstv
ms.assetid: 54ba8ca6-712f-46a1-9ed1-2b20ef8539ba
ms.date: 12/05/2018
ms.keywords: IIsdbComponentGroupDescriptor, IIsdbComponentGroupDescriptor interface [Microsoft TV Technologies], IIsdbComponentGroupDescriptor interface [Microsoft TV Technologies],described, dvbsiparser/IIsdbComponentGroupDescriptor, mstv.iisdbcomponentgroupdescriptor
ms.topic: interface
f1_keywords:
- dvbsiparser/IIsdbComponentGroupDescriptor
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
- IIsdbComponentGroupDescriptor
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IIsdbComponentGroupDescriptor interface


## -description


Implements methods that get data from an Integrated Services Digital Broadcasting (ISDB) component group descriptor. The component group  descriptor appears in the ISDB service information as part of the event information table (EIT) and describes component grouping in an event.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IIsdbComponentGroupDescriptor</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IIsdbComponentGroupDescriptor</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IIsdbComponentGroupDescriptor</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbcomponentgroupdescriptor-getcomponentgrouptype">GetComponentGroupType</a>
</td>
<td align="left" width="63%">
Gets the group type from   an ISDB component group descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbcomponentgroupdescriptor-getcountofrecords">GetCountOfRecords</a>
</td>
<td align="left" width="63%">
 Gets the number of component records in   an ISDB component group descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbcomponentgroupdescriptor-getlength">GetLength</a>
</td>
<td align="left" width="63%">
Gets the body length of  an ISDB component group descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbcomponentgroupdescriptor-getrecordcaunitcaunitid">GetRecordCAUnitCAUnitId</a>
</td>
<td align="left" width="63%">
Gets the identifier for a conditional access unit in   an ISDB component group descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbcomponentgroupdescriptor-getrecordcaunitcomponenttag">GetRecordCAUnitComponentTag</a>
</td>
<td align="left" width="63%">
Gets the identifier from a component record that  correspond to a conditional access in   an ISDB component group descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbcomponentgroupdescriptor-getrecordcaunitnumberofcomponents">GetRecordCAUnitNumberOfComponents</a>
</td>
<td align="left" width="63%">
  Gets the number of records that correspond to a conditional access unit in an ISDB component group descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbcomponentgroupdescriptor-getrecordgroupid">GetRecordGroupId</a>
</td>
<td align="left" width="63%">
Gets the record group identifier from  an ISDB component group descriptor. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbcomponentgroupdescriptor-getrecordnumberofcaunit">GetRecordNumberOfCAUnit</a>
</td>
<td align="left" width="63%">
  Gets the number of component records that correspond to a conditional access unit in an ISDB component group descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbcomponentgroupdescriptor-getrecordtextw">GetRecordTextW</a>
</td>
<td align="left" width="63%">
Gets the description of a component group from   an ISDB component group descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbcomponentgroupdescriptor-getrecordtotalbitrate">GetRecordTotalBitRate</a>
</td>
<td align="left" width="63%">
  Gets the total bit rate from a component record in an ISDB component group descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbcomponentgroupdescriptor-gettag">GetTag</a>
</td>
<td align="left" width="63%">
Gets the tag that identifies an ISDB component group descriptor.

</td>
</tr>
</table> 

