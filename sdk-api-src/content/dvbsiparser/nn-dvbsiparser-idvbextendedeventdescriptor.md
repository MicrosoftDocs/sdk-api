---
UID: NN:dvbsiparser.IDvbExtendedEventDescriptor
title: IDvbExtendedEventDescriptor (dvbsiparser.h)
author: windows-sdk-content
description: Implements methods that get data from a Digital Video Broadcast (DVB) extended event descriptor.
old-location: mstv\idvbextendedeventdescriptor.htm
tech.root: mstv
ms.assetid: db100f17-f7b8-4252-8090-44567ab9dcbe
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDvbExtendedEventDescriptor, IDvbExtendedEventDescriptor interface [Microsoft TV Technologies], IDvbExtendedEventDescriptor interface [Microsoft TV Technologies],described, dvbsiparser/IDvbExtendedEventDescriptor, mstv.idvbextendedeventdescriptor
ms.topic: interface
f1_keywords: 
 - "dvbsiparser/IDvbExtendedEventDescriptor"
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
 - IDvbExtendedEventDescriptor
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDvbExtendedEventDescriptor interface


## -description


Implements methods that get data  from a Digital Video Broadcast (DVB) extended event descriptor. An extended  event descriptor appears as part of the DVB service information in the event information table (EIT) and service information table (SIT). The descriptor provides a detailed text description of an event that may be used in addition to the
short event descriptor. More than one extended event descriptor can be associated to allow more than 256 bytes of information about one event
to be conveyed. Text information can be structured into two columns, one that provides an
item description field, and one that provides the item text, for example, to include a cast list in a movie or show description.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDvbExtendedEventDescriptor</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDvbExtendedEventDescriptor</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDvbExtendedEventDescriptor</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbextendedeventdescriptor-getconcatenateditemw">GetConcatenatedItemW</a>
</td>
<td align="left" width="63%">
Concatenates the bytes from the item in the current DVB extended event descriptor with the bytes from the item in the next DVB extended event descriptor and returns the concatenated data as a Unicode string.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbextendedeventdescriptor-getconcatenatedtextw">GetConcatenatedTextW</a>
</td>
<td align="left" width="63%">
Gets the concatenation of the text description in the current item with the text description in the next item of a DVB extended event descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbextendedeventdescriptor-getcountofrecords">GetCountOfRecords</a>
</td>
<td align="left" width="63%">
Gets the number of item descriptions  from a DVB extended event descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbextendedeventdescriptor-getdescriptornumber">GetDescriptorNumber</a>
</td>
<td align="left" width="63%">
Gets the descriptor number from a DVB extended event descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbextendedeventdescriptor-getlanguagecode">GetLanguageCode</a>
</td>
<td align="left" width="63%">
Gets the ISO 639 language identifier for the DVB extended event descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbextendedeventdescriptor-getlastdescriptornumber">GetLastDescriptorNumber</a>
</td>
<td align="left" width="63%">
Gets the number of the last descriptor associated with this descriptor from a DVB extended event descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbextendedeventdescriptor-getlength">GetLength</a>
</td>
<td align="left" width="63%">
Gets the body length of a DVB extended event descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbextendedeventdescriptor-getrecorditemrawbytes">GetRecordItemRawBytes</a>
</td>
<td align="left" width="63%">
Gets the raw data from the 
current item in a DVB extended event descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbextendedeventdescriptor-getrecorditemw">GetRecordItemW</a>
</td>
<td align="left" width="63%">
Gets the item and descriptor in Unicode string format from a  DVB extended event descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbextendedeventdescriptor-gettag">GetTag</a>
</td>
<td align="left" width="63%">
Gets the tag that identifies a Digital Video Broadcast (DVB) data broadcast descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbextendedeventdescriptor-gettextw">GetTextW</a>
</td>
<td align="left" width="63%">
Gets the text describing the event in Unicode string format from a DVB extended event descriptor.

</td>
</tr>
</table> 

