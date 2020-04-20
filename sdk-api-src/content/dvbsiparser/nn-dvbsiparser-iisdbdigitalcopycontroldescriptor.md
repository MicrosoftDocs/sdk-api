---
UID: NN:dvbsiparser.IIsdbDigitalCopyControlDescriptor
title: IIsdbDigitalCopyControlDescriptor (dvbsiparser.h)
description: Implements methods that get data from an Integrated Services Digital Broadcasting (ISDB) digital copy control descriptor.helpviewer_keywords: ["IIsdbDigitalCopyControlDescriptor","IIsdbDigitalCopyControlDescriptor interface [Microsoft TV Technologies]","IIsdbDigitalCopyControlDescriptor interface [Microsoft TV Technologies]","described","dvbsiparser/IIsdbDigitalCopyControlDescriptor","mstv.iisdbdigitalcopycontroldescriptor"]
old-location: mstv\iisdbdigitalcopycontroldescriptor.htm
tech.root: mstv
ms.assetid: d509eb58-0c58-4173-8c9c-d52b81932b5c
ms.date: 12/05/2018
ms.keywords: IIsdbDigitalCopyControlDescriptor, IIsdbDigitalCopyControlDescriptor interface [Microsoft TV Technologies], IIsdbDigitalCopyControlDescriptor interface [Microsoft TV Technologies],described, dvbsiparser/IIsdbDigitalCopyControlDescriptor, mstv.iisdbdigitalcopycontroldescriptor
f1_keywords:
- dvbsiparser/IIsdbDigitalCopyControlDescriptor
dev_langs:
- c++
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
- IIsdbDigitalCopyControlDescriptor
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IIsdbDigitalCopyControlDescriptor interface


## -description


Implements methods that get data from an Integrated Services Digital Broadcasting (ISDB) digital copy control descriptor. The digital copy control descriptor appears in the ISDB Service Information as part of the event information table (EIT). Broadcasting service
providers who hold copyrights can use this descriptor to provide data that controls the recording of digital broadcasts and provides copyright data for digital recording equipment. This descriptor also identifies the maximum transmission rate
for each event.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IIsdbDigitalCopyControlDescriptor</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IIsdbDigitalCopyControlDescriptor</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IIsdbDigitalCopyControlDescriptor</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbdigitalcopycontroldescriptor-getcopycontrol">GetCopyControl</a>
</td>
<td align="left" width="63%">
Gets a code that indicates copy control status from the main body of an ISDB digital copy control descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbdigitalcopycontroldescriptor-getcountofrecords">GetCountOfRecords</a>
</td>
<td align="left" width="63%">
Gets the number of records in  an ISDB digital copy control descriptor. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbdigitalcopycontroldescriptor-getlength">GetLength</a>
</td>
<td align="left" width="63%">
Gets the body length of an ISDB digital copy control descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbdigitalcopycontroldescriptor-getrecordcopycontrol">GetRecordCopyControl</a>
</td>
<td align="left" width="63%">
Gets a code that indicates copy control status from a record in an ISDB digital copy control descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbdigitalcopycontroldescriptor-gettag">GetTag</a>
</td>
<td align="left" width="63%">
Gets the tag that identifies an ISDB digital copy control descriptor.

</td>
</tr>
</table> 

