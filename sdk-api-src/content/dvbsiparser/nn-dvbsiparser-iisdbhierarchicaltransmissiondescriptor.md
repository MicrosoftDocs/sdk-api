---
UID: NN:dvbsiparser.IIsdbHierarchicalTransmissionDescriptor
title: IIsdbHierarchicalTransmissionDescriptor
author: windows-driver-content
description: Implements methods that get data from an Integrated Services Digital Broadcasting (ISDB) hierarchical transmission descriptor.
old-location: mstv\iisdbhierarchicaltransmissiondescriptor.htm
old-project: mstv
ms.assetid: 6586360b-60d8-4c3c-aa6e-b657e1784b6d
ms.author: windowsdriverdev
ms.date: 5/14/2018
ms.keywords: IIsdbHierarchicalTransmissionDescriptor, IIsdbHierarchicalTransmissionDescriptor interface [Microsoft TV Technologies], IIsdbHierarchicalTransmissionDescriptor interface [Microsoft TV Technologies],described, dvbsiparser/IIsdbHierarchicalTransmissionDescriptor, mstv.iisdbhierarchicaltransmissiondescriptor
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
-	IIsdbHierarchicalTransmissionDescriptor
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IIsdbHierarchicalTransmissionDescriptor interface


## -description


Implements methods that get data from an Integrated Services Digital Broadcasting (ISDB) hierarchical transmission descriptor. The hierarchical transmission descriptor appears as part of the ISDB service information in the program map table (PMT) and describes the relationship between hierarchical streams when events are transmitted hierarchically. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IIsdbHierarchicalTransmissionDescriptor</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IIsdbHierarchicalTransmissionDescriptor</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IIsdbHierarchicalTransmissionDescriptor</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/853885cf-36cc-402a-96a8-bc44701fc0a4">GetFutureUse1</a>
</td>
<td align="left" width="63%">
Gets the value of the 7-bit reserved_future_use field from an ISDB hierarchical transmission descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/19404536-3104-4ac7-a979-73236007d553">GetFutureUse2</a>
</td>
<td align="left" width="63%">
Gets the value of the 3-bit reserved_future_use field from an ISDB hierarchical transmission descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/de183193-09b7-4774-9640-f02ec597d9c6">GetLength</a>
</td>
<td align="left" width="63%">
Gets the body length of an ISDB hierarchical transmission descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4890c3aa-487f-41c7-9202-636ded2ec46b">GetQualityLevel</a>
</td>
<td align="left" width="63%">
Gets a flag that indicates the quality level of the hierarchical stream construction from an ISDB hierarchical transmission descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4c1d96eb-e2d6-4f3a-8a3c-88c0d920ad44">GetReferencePid</a>
</td>
<td align="left" width="63%">
Gets the program ID (PID) of the primary hierarchical stream from an ISDB hierarchical transmission descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1aed2424-567b-4a6b-ae32-b3c74ce75026">GetTag</a>
</td>
<td align="left" width="63%">
Gets the tag that identifies an ISDB hierarchical transmission descriptor.

</td>
</tr>
</table> 

