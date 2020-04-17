---
UID: NN:dvbsiparser.IDvbComponentDescriptor
title: IDvbComponentDescriptor (dvbsiparser.h)
description: Identifies the type of a Digital Video Broadcast (DVB) component stream and provides a text description of the component stream.helpviewer_keywords: ["IDvbComponentDescriptor","IDvbComponentDescriptor interface [Microsoft TV Technologies]","IDvbComponentDescriptor interface [Microsoft TV Technologies]","described","dvbsiparser/IDvbComponentDescriptor","mstv.idvbcomponentdescriptor"]
old-location: mstv\idvbcomponentdescriptor.htm
tech.root: mstv
ms.assetid: 0dee15ee-5b36-4454-8092-6b57ef5063ce
ms.date: 12/05/2018
ms.keywords: IDvbComponentDescriptor, IDvbComponentDescriptor interface [Microsoft TV Technologies], IDvbComponentDescriptor interface [Microsoft TV Technologies],described, dvbsiparser/IDvbComponentDescriptor, mstv.idvbcomponentdescriptor
f1_keywords:
- dvbsiparser/IDvbComponentDescriptor
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
- IDvbComponentDescriptor
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDvbComponentDescriptor interface


## -description


Identifies the type of a Digital Video Broadcast (DVB) component stream and provides a text description of the component stream.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDvbComponentDescriptor</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDvbComponentDescriptor</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDvbComponentDescriptor</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbcomponentdescriptor-getcomponenttag">GetComponentTag</a>
</td>
<td align="left" width="63%">
Gets the component tag from  a DVB component descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbcomponentdescriptor-getcomponenttype">GetComponentType</a>
</td>
<td align="left" width="63%">
 Gets the component type code for a DVB component descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbcomponentdescriptor-getlanguagecode">GetLanguageCode</a>
</td>
<td align="left" width="63%">
Gets the ISO 639 language identifier for a DVB component descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbcomponentdescriptor-getlength">GetLength</a>
</td>
<td align="left" width="63%">
Gets the body length of a  a DVB component descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbcomponentdescriptor-getstreamcontent">GetStreamContent</a>
</td>
<td align="left" width="63%">
 Gets the stream content code for a DVB component descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbcomponentdescriptor-gettag">GetTag</a>
</td>
<td align="left" width="63%">
Gets the tag that identifies a DVB component descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbcomponentdescriptor-gettextw">GetTextW</a>
</td>
<td align="left" width="63%">
 Gets the text describing the elementary stream  from a DVB component descriptor, in Unicode string format.

</td>
</tr>
</table> 

