---
UID: NN:dvbsiparser.IIsdbEventGroupDescriptor
title: IIsdbEventGroupDescriptor (dvbsiparser.h)
author: windows-sdk-content
description: Implements methods that get data from an Integrated Services Digital Broadcasting (ISDB) event group descriptor.
old-location: mstv\iisdbeventgroupdescriptor.htm
tech.root: mstv
ms.assetid: 1e71f277-0296-4589-8099-dfae2a9dcfb0
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IIsdbEventGroupDescriptor, IIsdbEventGroupDescriptor interface [Microsoft TV Technologies], IIsdbEventGroupDescriptor interface [Microsoft TV Technologies],described, dvbsiparser/IIsdbEventGroupDescriptor, mstv.iisdbeventgroupdescriptor
ms.topic: interface
f1_keywords: 
 - "dvbsiparser/IIsdbEventGroupDescriptor"
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
 - IIsdbEventGroupDescriptor
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IIsdbEventGroupDescriptor interface


## -description


Implements methods that get data from an Integrated Services Digital Broadcasting (ISDB) event group descriptor. The event group  descriptor appears in the ISDB service information as part of the event information table (EIT) and describes a group of related events. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IIsdbEventGroupDescriptor</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IIsdbEventGroupDescriptor</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IIsdbEventGroupDescriptor</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbeventgroupdescriptor-getcountofrecords">GetCountOfRecords</a>
</td>
<td align="left" width="63%">
 Gets the number of event records in   an ISDB event group descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbeventgroupdescriptor-getcountofrefrecords">GetCountOfRefRecords</a>
</td>
<td align="left" width="63%">
 Gets the number of records for related events from an ISDB event group descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbeventgroupdescriptor-getgrouptype">GetGroupType</a>
</td>
<td align="left" width="63%">
 Gets a code that describes the group type from an ISDB event group descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbeventgroupdescriptor-getlength">GetLength</a>
</td>
<td align="left" width="63%">
Gets the body length of  an ISDB event group descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbeventgroupdescriptor-getrecordevent">GetRecordEvent</a>
</td>
<td align="left" width="63%">
 Gets data from an event record in an ISDB event group descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbeventgroupdescriptor-getrefrecordevent">GetRefRecordEvent</a>
</td>
<td align="left" width="63%">
 Gets data from a related event record in an ISDB event group descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbeventgroupdescriptor-gettag">GetTag</a>
</td>
<td align="left" width="63%">
 Gets the tag that identifies an ISDB event group descriptor.

</td>
</tr>
</table> 

