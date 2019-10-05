---
UID: NN:dvbsiparser.IIsdbHierarchicalTransmissionDescriptor
title: IIsdbHierarchicalTransmissionDescriptor (dvbsiparser.h)
author: windows-sdk-content
description: Implements methods that get data from an Integrated Services Digital Broadcasting (ISDB) hierarchical transmission descriptor.
old-location: mstv\iisdbhierarchicaltransmissiondescriptor.htm
tech.root: mstv
ms.assetid: 6586360b-60d8-4c3c-aa6e-b657e1784b6d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IIsdbHierarchicalTransmissionDescriptor, IIsdbHierarchicalTransmissionDescriptor interface [Microsoft TV Technologies], IIsdbHierarchicalTransmissionDescriptor interface [Microsoft TV Technologies],described, dvbsiparser/IIsdbHierarchicalTransmissionDescriptor, mstv.iisdbhierarchicaltransmissiondescriptor
ms.topic: interface
f1_keywords: 
 - "dvbsiparser/IIsdbHierarchicalTransmissionDescriptor"
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
 - IIsdbHierarchicalTransmissionDescriptor
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IIsdbHierarchicalTransmissionDescriptor interface


## -description


Implements methods that get data from an Integrated Services Digital Broadcasting (ISDB) hierarchical transmission descriptor. The hierarchical transmission descriptor appears as part of the ISDB service information in the program map table (PMT) and describes the relationship between hierarchical streams when events are transmitted hierarchically. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IIsdbHierarchicalTransmissionDescriptor</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IIsdbHierarchicalTransmissionDescriptor</b> also has these types of members:
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
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbhierarchicaltransmissiondescriptor-getfutureuse1">GetFutureUse1</a>
</td>
<td align="left" width="63%">
Gets the value of the 7-bit reserved_future_use field from an ISDB hierarchical transmission descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbhierarchicaltransmissiondescriptor-getfutureuse2">GetFutureUse2</a>
</td>
<td align="left" width="63%">
Gets the value of the 3-bit reserved_future_use field from an ISDB hierarchical transmission descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbhierarchicaltransmissiondescriptor-getlength">GetLength</a>
</td>
<td align="left" width="63%">
Gets the body length of an ISDB hierarchical transmission descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbhierarchicaltransmissiondescriptor-getqualitylevel">GetQualityLevel</a>
</td>
<td align="left" width="63%">
Gets a flag that indicates the quality level of the hierarchical stream construction from an ISDB hierarchical transmission descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbhierarchicaltransmissiondescriptor-getreferencepid">GetReferencePid</a>
</td>
<td align="left" width="63%">
Gets the program ID (PID) of the primary hierarchical stream from an ISDB hierarchical transmission descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbhierarchicaltransmissiondescriptor-gettag">GetTag</a>
</td>
<td align="left" width="63%">
Gets the tag that identifies an ISDB hierarchical transmission descriptor.

</td>
</tr>
</table> 

