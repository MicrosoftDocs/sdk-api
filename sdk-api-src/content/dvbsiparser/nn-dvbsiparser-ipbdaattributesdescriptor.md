---
UID: NN:dvbsiparser.IPBDAAttributesDescriptor
title: IPBDAAttributesDescriptor (dvbsiparser.h)
description: Implements methods that get data from anattributes descriptor in a Protected Broadcast Device Architecture (PBDA) transport stream.
old-location: mstv\ipbdaattributesdescriptor.htm
tech.root: mstv
ms.assetid: 489348b7-0f10-4a49-a7d4-10a1ed478aa8
ms.date: 12/05/2018
ms.keywords: IPBDAAttributesDescriptor, IPBDAAttributesDescriptor interface [Microsoft TV Technologies], IPBDAAttributesDescriptor interface [Microsoft TV Technologies],described, dvbsiparser/IPBDAAttributesDescriptor, mstv.ipbdaattributesdescriptor
f1_keywords:
- dvbsiparser/IPBDAAttributesDescriptor
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
- IPBDAAttributesDescriptor
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IPBDAAttributesDescriptor interface


## -description


Implements methods that get data from anattributes descriptor in a Protected Broadcast  Device Architecture (PBDA) transport stream.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPBDAAttributesDescriptor</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IPBDAAttributesDescriptor</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IPBDAAttributesDescriptor</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-ipbdaattributesdescriptor-getattributepayload">GetAttributePayload</a>
</td>
<td align="left" width="63%">
Gets the descriptor body from the attributes descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-ipbdaattributesdescriptor-getlength">GetLength</a>
</td>
<td align="left" width="63%">
Gets the body length of the  attributes descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-ipbdaattributesdescriptor-gettag">GetTag</a>
</td>
<td align="left" width="63%">
Gets the tag that uniquely identifies the attributes descriptor.

</td>
</tr>
</table> 

