---
UID: NN:dvbsiparser.IIsdbSeriesDescriptor
title: IIsdbSeriesDescriptor (dvbsiparser.h)
author: windows-sdk-content
description: Implements methods that get data from an Integrated Services Digital Broadcasting (ISDB) series descriptor.
old-location: mstv\iisdbseriesdescriptor.htm
tech.root: mstv
ms.assetid: 07c4debc-1817-46ac-9f67-9b8637a04662
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IIsdbSeriesDescriptor, IIsdbSeriesDescriptor interface [Microsoft TV Technologies], IIsdbSeriesDescriptor interface [Microsoft TV Technologies],described, dvbsiparser/IIsdbSeriesDescriptor, mstv.iisdbseriesdescriptor
ms.topic: interface
f1_keywords: 
 - "dvbsiparser/IIsdbSeriesDescriptor"
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
 - IIsdbSeriesDescriptor
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IIsdbSeriesDescriptor interface


## -description


Implements methods that get data from an Integrated Services Digital Broadcasting (ISDB) series descriptor. The series descriptor appears in the ISDB Service Information as part of the event information table (EIT) and defines series information among multiple events.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IIsdbSeriesDescriptor</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IIsdbSeriesDescriptor</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IIsdbSeriesDescriptor</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbseriesdescriptor-getepisodenumber">GetEpisodeNumber</a>
</td>
<td align="left" width="63%">
 Gets the episode number of a series from an ISDB series descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbseriesdescriptor-getexpiredate">GetExpireDate</a>
</td>
<td align="left" width="63%">
Gets a date that identifies the end date of a series from  an ISDB series descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbseriesdescriptor-getlastepisodenumber">GetLastEpisodeNumber</a>
</td>
<td align="left" width="63%">
 Gets the number of the final episode of a series from an ISDB series descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbseriesdescriptor-getlength">GetLength</a>
</td>
<td align="left" width="63%">
Gets the body length of  an ISDB series descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbseriesdescriptor-getprogrampattern">GetProgramPattern</a>
</td>
<td align="left" width="63%">
 Gets a code that identifies the how often a series is broadcast from an ISDB series descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbseriesdescriptor-getrepeatlabel">GetRepeatLabel</a>
</td>
<td align="left" width="63%">
 Gets the label that identifies repeat broadcasts of a series from ISDB series descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbseriesdescriptor-getseriesid">GetSeriesId</a>
</td>
<td align="left" width="63%">
 Gets the series identifier from an ISDB series descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbseriesdescriptor-getseriesnamew">GetSeriesNameW</a>
</td>
<td align="left" width="63%">
 Gets the name of the series from an ISDB series descriptor, in Unicode string format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbseriesdescriptor-gettag">GetTag</a>
</td>
<td align="left" width="63%">
Gets the tag that identifies an ISDB series descriptor.

</td>
</tr>
</table> 

