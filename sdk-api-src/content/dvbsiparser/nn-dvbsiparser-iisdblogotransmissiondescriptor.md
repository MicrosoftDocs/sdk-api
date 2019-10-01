---
UID: NN:dvbsiparser.IIsdbLogoTransmissionDescriptor
title: IIsdbLogoTransmissionDescriptor (dvbsiparser.h)
author: windows-sdk-content
description: Implements methods that get data from an Integrated Services Digital Broadcasting (ISDB) logo transmission descriptor.
old-location: mstv\iisdblogotransmissiondescriptor.htm
tech.root: mstv
ms.assetid: 9c0930f6-6c05-48c9-91e4-2abdd3355a32
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IIsdbLogoTransmissionDescriptor, IIsdbLogoTransmissionDescriptor interface [Microsoft TV Technologies], IIsdbLogoTransmissionDescriptor interface [Microsoft TV Technologies],described, dvbsiparser/IIsdbLogoTransmissionDescriptor, mstv.iisdblogotransmissiondescriptor
ms.topic: interface
f1_keywords: 
 - "dvbsiparser/IIsdbLogoTransmissionDescriptor"
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
 - IIsdbLogoTransmissionDescriptor
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IIsdbLogoTransmissionDescriptor interface


## -description


Implements methods that get data from an Integrated Services Digital Broadcasting (ISDB) logo transmission descriptor. The logo transmission descriptor appears in the ISDB Service Information as part of the service description table (SDT) and contains information required for transmission of logos.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IIsdbLogoTransmissionDescriptor</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IIsdbLogoTransmissionDescriptor</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IIsdbLogoTransmissionDescriptor</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdblogotransmissiondescriptor-getdownloaddataid">GetDownloadDataId</a>
</td>
<td align="left" width="63%">
Gets the identifier for the downloaded data from an ISDB logo transmission descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdblogotransmissiondescriptor-getlength">GetLength</a>
</td>
<td align="left" width="63%">
Gets the body length of  an ISDB logo transmission descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdblogotransmissiondescriptor-getlogocharw">GetLogoCharW</a>
</td>
<td align="left" width="63%">
Gets the character string for a simple logo from an ISDB logo transmission descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdblogotransmissiondescriptor-getlogoid">GetLogoId</a>
</td>
<td align="left" width="63%">
 Gets the logo identifier from an ISDB logo transmission descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdblogotransmissiondescriptor-getlogotransmissiontype">GetLogoTransmissionType</a>
</td>
<td align="left" width="63%">
Gets the logo transmission type from an ISDB logo transmission descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdblogotransmissiondescriptor-getlogoversion">GetLogoVersion</a>
</td>
<td align="left" width="63%">
 Gets the version number for a logo from an ISDB logo transmission descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdblogotransmissiondescriptor-gettag">GetTag</a>
</td>
<td align="left" width="63%">
Gets the tag that identifies an ISDB logo transmission descriptor.

</td>
</tr>
</table> 

