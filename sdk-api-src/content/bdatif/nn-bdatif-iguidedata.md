---
UID: NN:bdatif.IGuideData
title: IGuideData (bdatif.h)
description: The IGuideData interface is exposed by the BDA MPEG-2 Transport Information Filter (TIF). It enables the client to get service information from the MPEG-2 transport stream. Use this interface if you are writing a guide store loader.
helpviewer_keywords: ["IGuideData","IGuideData interface [Microsoft TV Technologies]","IGuideData interface [Microsoft TV Technologies]","described","IGuideDataInterface","bdatif/IGuideData","mstv.iguidedata"]
old-location: mstv\iguidedata.htm
tech.root: mstv
ms.assetid: 3bd27fce-90be-480b-b157-a17beccda068
ms.date: 12/05/2018
ms.keywords: IGuideData, IGuideData interface [Microsoft TV Technologies], IGuideData interface [Microsoft TV Technologies],described, IGuideDataInterface, bdatif/IGuideData, mstv.iguidedata
req.header: bdatif.h
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IGuideData
 - bdatif/IGuideData
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Bdatif.h
api_name:
 - IGuideData
---

# IGuideData interface


## -description

The <b>IGuideData</b> interface is exposed by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/bda-mpeg-2-transport-information-filter">BDA MPEG-2 Transport Information Filter</a> (TIF). It enables the client to get service information from the MPEG-2 transport stream. Use this interface if you are writing a guide store loader.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IGuideData</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IGuideData</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IGuideData</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/bdatif/nf-bdatif-iguidedata-getguideprogramids">GetGuideProgramIDs</a>
</td>
<td align="left" width="63%">
Returns a list of unique identifiers for all of the programs contained in all transport streams.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/bdatif/nf-bdatif-iguidedata-getprogramproperties">GetProgramProperties</a>
</td>
<td align="left" width="63%">
Retrieves the properties for a specified program.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/bdatif/nf-bdatif-iguidedata-getscheduleentryids">GetScheduleEntryIDs</a>
</td>
<td align="left" width="63%">
Returns a list of unique identifiers for all of the schedule entries contained in all transport streams.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/bdatif/nf-bdatif-iguidedata-getscheduleentryproperties">GetScheduleEntryProperties</a>
</td>
<td align="left" width="63%">
Retrieves the properties for a specified schedule entry.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/bdatif/nf-bdatif-iguidedata-getserviceproperties">GetServiceProperties</a>
</td>
<td align="left" width="63%">
Retrieves the properties for a specified service.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/bdatif/nf-bdatif-iguidedata-getservices">GetServices</a>
</td>
<td align="left" width="63%">
Retrieves a collection of tune requests representing all of the services available in the tuning space.

</td>
</tr>
</table>

## -remarks

The TIF collects service informaton for services, programs, and schedule entries. A service is analogous to a channel; a program is a television show (also known as an "event"); and a schedule entry is an event that occurs at a specific time on a specific service.

For each program and schedule entry, the TIF creates a string that uniquely identifies that element within the multiplex. The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/bdatif/nf-bdatif-iguidedata-getguideprogramids">GetGuideProgramIDs</a> and <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/bdatif/nf-bdatif-iguidedata-getscheduleentryids">GetScheduleEntryIDs</a> methods return a list of these identifiers. You can then pass the identifier to the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/bdatif/nf-bdatif-iguidedata-getprogramproperties">GetProgramProperties</a> and <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/bdatif/nf-bdatif-iguidedata-getscheduleentryproperties">GetScheduleEntryProperties</a> methods to get additional properties for a particular element.

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IGuideData)</code>.

## -see-also

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/bda-interfaces">BDA Interfaces</a>

