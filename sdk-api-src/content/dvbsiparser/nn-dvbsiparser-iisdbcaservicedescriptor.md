---
UID: NN:dvbsiparser.IIsdbCAServiceDescriptor
title: IIsdbCAServiceDescriptor (dvbsiparser.h)
description: Implements methods that get data from an Integrated Services Digital Broadcasting (ISDB) conditional access (CA) service descriptor.
helpviewer_keywords: ["IIsdbCAServiceDescriptor","IIsdbCAServiceDescriptor interface [Microsoft TV Technologies]","IIsdbCAServiceDescriptor interface [Microsoft TV Technologies]","described","dvbsiparser/IIsdbCAServiceDescriptor","mstv.iisdbcaservicedescriptor"]
old-location: mstv\iisdbcaservicedescriptor.htm
tech.root: mstv
ms.assetid: 6d56e39d-3c7a-4c55-8d07-00e25eba18bd
ms.date: 12/05/2018
ms.keywords: IIsdbCAServiceDescriptor, IIsdbCAServiceDescriptor interface [Microsoft TV Technologies], IIsdbCAServiceDescriptor interface [Microsoft TV Technologies],described, dvbsiparser/IIsdbCAServiceDescriptor, mstv.iisdbcaservicedescriptor
f1_keywords:
- dvbsiparser/IIsdbCAServiceDescriptor
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
- IIsdbCAServiceDescriptor
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IIsdbCAServiceDescriptor interface


## -description


Implements methods that get data from  an Integrated Services Digital Broadcasting (ISDB) conditional access (CA) service descriptor. The conditional access service descriptor appears in the ISDB service information as part of the conditional access table (CAT). It facilitates the display of  entitlement management message (EMM) automatic display
messages by indicating the broadcaster group that provides the service, the EMM automatic
display message, and the delay time for displaying the "EMM automatic display message" .


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IIsdbCAServiceDescriptor</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IIsdbCAServiceDescriptor</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IIsdbCAServiceDescriptor</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbcaservicedescriptor-getcabroadcastergroupid">GetCABroadcasterGroupId</a>
</td>
<td align="left" width="63%">
Gets the broadcaster group identifier from an ISDB CA service descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbcaservicedescriptor-getcasystemid">GetCASystemId</a>
</td>
<td align="left" width="63%">
Gets the system identifier from an ISDB CA service descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbcaservicedescriptor-getlength">GetLength</a>
</td>
<td align="left" width="63%">
Gets the body length of an ISDB CA service descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbcaservicedescriptor-getmessagecontrol">GetMessageControl</a>
</td>
<td align="left" width="63%">
Gets the delay time before the automatic EMM message is displayed from an ISDB CA service descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbcaservicedescriptor-getserviceids">GetServiceIds</a>
</td>
<td align="left" width="63%">
Gets service identifiers from an ISDB CA service descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbcaservicedescriptor-gettag">GetTag</a>
</td>
<td align="left" width="63%">
Gets the tag that identifies an ISDB CA service descriptor.

</td>
</tr>
</table> 

