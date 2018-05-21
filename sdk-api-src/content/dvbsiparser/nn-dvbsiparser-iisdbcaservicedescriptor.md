---
UID: NN:dvbsiparser.IIsdbCAServiceDescriptor
title: IIsdbCAServiceDescriptor
author: windows-driver-content
description: Implements methods that get data from an Integrated Services Digital Broadcasting (ISDB) conditional access (CA) service descriptor.
old-location: mstv\iisdbcaservicedescriptor.htm
old-project: mstv
ms.assetid: 6d56e39d-3c7a-4c55-8d07-00e25eba18bd
ms.author: windowsdriverdev
ms.date: 5/14/2018
ms.keywords: IIsdbCAServiceDescriptor, IIsdbCAServiceDescriptor interface [Microsoft TV Technologies], IIsdbCAServiceDescriptor interface [Microsoft TV Technologies],described, dvbsiparser/IIsdbCAServiceDescriptor, mstv.iisdbcaservicedescriptor
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
req.typenames: DSROLE_UPGRADE_STATUS_INFO, *PDSROLE_UPGRADE_STATUS_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	dvbsiparser.h
api_name:
-	IIsdbCAServiceDescriptor
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IIsdbCAServiceDescriptor interface


## -description


Implements methods that get data from  an Integrated Services Digital Broadcasting (ISDB) conditional access (CA) service descriptor. The conditional access service descriptor appears in the ISDB service information as part of the conditional access table (CAT). It facilitates the display of  entitlement management message (EMM) automatic display
messages by indicating the broadcaster group that provides the service, the EMM automatic
display message, and the delay time for displaying the "EMM automatic display message" .


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IIsdbCAServiceDescriptor</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IIsdbCAServiceDescriptor</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/cc783e34-3544-4bcf-9e76-cb098c89cd65">GetCABroadcasterGroupId</a>
</td>
<td align="left" width="63%">
Gets the broadcaster group identifier from an ISDB CA service descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/48148c5c-30e1-4028-8baf-692141d79fad">GetCASystemId</a>
</td>
<td align="left" width="63%">
Gets the system identifier from an ISDB CA service descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dfa6a372-8e9f-4f38-80ea-ad27c9423cc5">GetLength</a>
</td>
<td align="left" width="63%">
Gets the body length of an ISDB CA service descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0a911c5e-a026-4d35-a6a2-e33ba53f3057">GetMessageControl</a>
</td>
<td align="left" width="63%">
Gets the delay time before the automatic EMM message is displayed from an ISDB CA service descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f2a6d1f2-2cd5-4f8c-97e1-33880ffb0449">GetServiceIds</a>
</td>
<td align="left" width="63%">
Gets service identifiers from an ISDB CA service descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/55f7b955-03f6-4c40-bd73-175bf3453ed0">GetTag</a>
</td>
<td align="left" width="63%">
Gets the tag that identifies an ISDB CA service descriptor.

</td>
</tr>
</table> 

