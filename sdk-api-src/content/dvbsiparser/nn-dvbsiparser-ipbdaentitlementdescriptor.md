---
UID: NN:dvbsiparser.IPBDAEntitlementDescriptor
title: IPBDAEntitlementDescriptor (dvbsiparser.h)
description: Implements methods that retrieve data from the entitlement descriptor in a Protected Broadcast Driver Architecture (PBDA) transport stream.helpviewer_keywords: ["IPBDAEntitlementDescriptor","IPBDAEntitlementDescriptor interface [Microsoft TV Technologies]","IPBDAEntitlementDescriptor interface [Microsoft TV Technologies]","described","dvbsiparser/IPBDAEntitlementDescriptor","mstv.ipbdaentitlementdescriptor"]
old-location: mstv\ipbdaentitlementdescriptor.htm
tech.root: mstv
ms.assetid: 2fe666fa-ebc4-4a47-87ce-085f357ce186
ms.date: 12/05/2018
ms.keywords: IPBDAEntitlementDescriptor, IPBDAEntitlementDescriptor interface [Microsoft TV Technologies], IPBDAEntitlementDescriptor interface [Microsoft TV Technologies],described, dvbsiparser/IPBDAEntitlementDescriptor, mstv.ipbdaentitlementdescriptor
f1_keywords:
- dvbsiparser/IPBDAEntitlementDescriptor
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
- IPBDAEntitlementDescriptor
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IPBDAEntitlementDescriptor interface


## -description


Implements methods that retrieve data from the entitlement descriptor in a Protected Broadcast Driver Architecture (PBDA) transport stream.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPBDAEntitlementDescriptor</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IPBDAEntitlementDescriptor</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IPBDAEntitlementDescriptor</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-ipbdaentitlementdescriptor-getlength">GetLength</a>
</td>
<td align="left" width="63%">
Gets the body length of the entitlement descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-ipbdaentitlementdescriptor-gettag">GetTag</a>
</td>
<td align="left" width="63%">
Gets the tag that uniquely identifies the entitlement descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-ipbdaentitlementdescriptor-gettoken">GetToken</a>
</td>
<td align="left" width="63%">
Gets the entitlement token from the entitlement descriptor.

</td>
</tr>
</table> 

