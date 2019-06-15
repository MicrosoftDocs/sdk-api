---
UID: NN:dvbsiparser.IIsdbDataContentDescriptor
title: IIsdbDataContentDescriptor (dvbsiparser.h)
author: windows-sdk-content
description: Implements methods that get data from an Integrated Services Digital Broadcasting (ISDB) data content descriptor.
old-location: mstv\iisdbdatacontentdescriptor.htm
tech.root: mstv
ms.assetid: 91d55991-5994-4104-9a8f-01cfc347a96f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IIsdbDatacontentDescriptor, IIsdbDatacontentDescriptor interface [Microsoft TV Technologies], IIsdbDatacontentDescriptor interface [Microsoft TV Technologies],described, dvbsiparser/IIsdbDatacontentDescriptor, mstv.iisdbdatacontentdescriptor
ms.topic: interface
f1_keywords: ["dvbsiparser/IIsdbDatacontentDescriptor"]
req.header: dvbsiparser.h
req.include-header: 
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
 - Dvbsiparser.h
api_name:
 - IIsdbDatacontentDescriptor
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IIsdbDataContentDescriptor interface


## -description


Implements methods that get data from an Integrated Services Digital Broadcasting (ISDB) data content descriptor. The data content descriptor appears in the ISDB Service Information as part of the event information table (EIT) and provides details about the content of a data broadcasting event.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IIsdbDatacontentDescriptor</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IIsdbDatacontentDescriptor</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IIsdbDatacontentDescriptor</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbdatacontentdescriptor-getcountofrecords">GetCountOfRecords</a>
</td>
<td align="left" width="63%">
 Gets the number of component records in  an ISDB data content descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbdatacontentdescriptor-getdatacomponentid">GetDataComponentId</a>
</td>
<td align="left" width="63%">
 Gets a component identifier from an ISDB data content descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbdatacontentdescriptor-getentrycomponent">GetEntryComponent</a>
</td>
<td align="left" width="63%">
 Gets a code that indicates the first referenced component stream in the descriptor from an ISDB data content descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbdatacontentdescriptor-getlanguagecode">GetLanguageCode</a>
</td>
<td align="left" width="63%">
Gets the three-character ISO 639 language code from an ISDB data content descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbdatacontentdescriptor-getlength">GetLength</a>
</td>
<td align="left" width="63%">
 Gets the body length of an ISDB data content descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbdatacontentdescriptor-getrecordcomponentref">GetRecordComponentRef</a>
</td>
<td align="left" width="63%">
Gets a broadcaster-defined component tag that identifies a component stream from ISDB data content descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbdatacontentdescriptor-getselectorbytes">GetSelectorBytes</a>
</td>
<td align="left" width="63%">
 Gets data from the selector area of an ISDB data content descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbdatacontentdescriptor-getselectorlength">GetSelectorLength</a>
</td>
<td align="left" width="63%">
Gets the length of the selector area from an ISDB data content descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbdatacontentdescriptor-gettag">GetTag</a>
</td>
<td align="left" width="63%">
Gets the tag that identifies an ISDB data content descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbdatacontentdescriptor-gettextw">GetTextW</a>
</td>
<td align="left" width="63%">
 Gets the text that describes a component in an ISDB data content descriptor, in Unicode text format.

</td>
</tr>
</table> 

