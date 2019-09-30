---
UID: NN:dvbsiparser.IIsdbDownloadContentDescriptor
title: IIsdbDownloadContentDescriptor (dvbsiparser.h)
author: windows-sdk-content
description: Implements methods that get data from an Integrated Services Digital Broadcasting (ISDB) download content descriptor.
old-location: mstv\iisdbdownloadcontentdescriptor.htm
tech.root: mstv
ms.assetid: beef626c-64b1-4f49-bb21-69022907004d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IIsdbDownloadContentDescriptor, IIsdbDownloadContentDescriptor interface [Microsoft TV Technologies], IIsdbDownloadContentDescriptor interface [Microsoft TV Technologies],described, dvbsiparser/IIsdbDownloadContentDescriptor, mstv.iisdbdownloadcontentdescriptor
ms.topic: interface
f1_keywords: 
 - "dvbsiparser/IIsdbDownloadContentDescriptor"
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
 - IIsdbDownloadContentDescriptor
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IIsdbDownloadContentDescriptor interface


## -description


Implements methods that get data from an Integrated Services Digital Broadcasting (ISDB) download content descriptor. The download content descriptor appears in the ISDB Service Information as part of the software download trigger table (SDTT) and provides details about content and scheduling related to downloading.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IIsdbDownloadContentDescriptor</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IIsdbDownloadContentDescriptor</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IIsdbDownloadContentDescriptor</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbdownloadcontentdescriptor-getcompatiblitydescriptor">GetCompatiblityDescriptor</a>
</td>
<td align="left" width="63%">
Gets data from the compatibility descriptor in an ISDB download content descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbdownloadcontentdescriptor-getcompatiblitydescriptorlength">GetCompatiblityDescriptorLength</a>
</td>
<td align="left" width="63%">
Gets the length of the compatibility descriptor  from an ISDB download content descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbdownloadcontentdescriptor-getcomponentsize">GetComponentSize</a>
</td>
<td align="left" width="63%">
 Gets the total size of components within an ISDB download content descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbdownloadcontentdescriptor-getcomponenttag">GetComponentTag</a>
</td>
<td align="left" width="63%">
 Gets a tag that identifies the downloaded stream from an ISDB download content descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbdownloadcontentdescriptor-getcountofrecords">GetCountOfRecords</a>
</td>
<td align="left" width="63%">
Gets the number of records in an ISDB download content descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbdownloadcontentdescriptor-getdownloadid">GetDownloadId</a>
</td>
<td align="left" width="63%">
 Gets the download identifier from an ISDB download content descriptor

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbdownloadcontentdescriptor-getflags">GetFlags</a>
</td>
<td align="left" width="63%">
Gets the values of flags  from an ISDB download content descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbdownloadcontentdescriptor-getleakrate">GetLeakRate</a>
</td>
<td align="left" width="63%">
 Gets the leak rate of the transport buffer from an ISDB download content descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbdownloadcontentdescriptor-getlength">GetLength</a>
</td>
<td align="left" width="63%">
Gets the body length of an ISDB download content descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbdownloadcontentdescriptor-getrecordmoduleid">GetRecordModuleId</a>
</td>
<td align="left" width="63%">
 Gets the identifier for a carousel module from an ISDB download content descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbdownloadcontentdescriptor-getrecordmoduleinfo">GetRecordModuleInfo</a>
</td>
<td align="left" width="63%">
Gets the module descriptor field from an ISDB download content descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbdownloadcontentdescriptor-getrecordmoduleinfolength">GetRecordModuleInfoLength</a>
</td>
<td align="left" width="63%">
 Gets the length of the module_info_byte field that contains descriptors for the module from an ISDB download content descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbdownloadcontentdescriptor-getrecordmodulesize">GetRecordModuleSize</a>
</td>
<td align="left" width="63%">
 Gets the size of a carousel module from an ISDB download content descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbdownloadcontentdescriptor-gettag">GetTag</a>
</td>
<td align="left" width="63%">
Gets the tag that identifies an ISDB download content descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbdownloadcontentdescriptor-gettextlanguagecode">GetTextLanguageCode</a>
</td>
<td align="left" width="63%">
 Gets the three-character ISO 639 language code used for the service description in an ISDB download content descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbdownloadcontentdescriptor-gettextw">GetTextW</a>
</td>
<td align="left" width="63%">
 Gets the service description from an ISDB download content descriptor, in Unicode string format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbdownloadcontentdescriptor-gettimeoutvaluedii">GetTimeOutValueDII</a>
</td>
<td align="left" width="63%">
 Gets the recommended download timeout interval from an ISDB download content descriptor.

</td>
</tr>
</table> 

