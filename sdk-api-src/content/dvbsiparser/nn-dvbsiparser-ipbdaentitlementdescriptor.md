---
UID: NN:dvbsiparser.IPBDAEntitlementDescriptor
title: IPBDAEntitlementDescriptor
author: windows-sdk-content
description: Implements methods that retrieve data from the entitlement descriptor in a Protected Broadcast Driver Architecture (PBDA) transport stream.
old-location: mstv\ipbdaentitlementdescriptor.htm
old-project: mstv
ms.assetid: 2fe666fa-ebc4-4a47-87ce-085f357ce186
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IPBDAEntitlementDescriptor, IPBDAEntitlementDescriptor interface [Microsoft TV Technologies], IPBDAEntitlementDescriptor interface [Microsoft TV Technologies],described, dvbsiparser/IPBDAEntitlementDescriptor, mstv.ipbdaentitlementdescriptor
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: DSROLE_UPGRADE_STATUS_INFO, *PDSROLE_UPGRADE_STATUS_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dvbsiparser.h
api_name:
 - IPBDAEntitlementDescriptor
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IPBDAEntitlementDescriptor interface


## -description


Implements methods that retrieve data from the entitlement descriptor in a Protected Broadcast Driver Architecture (PBDA) transport stream.

For more information about PBDA, download the specification from <a href="http://go.microsoft.com/fwlink/p/?linkid=132926">http://go.microsoft.com/fwlink/p/?linkid=132926</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPBDAEntitlementDescriptor</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IPBDAEntitlementDescriptor</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/51fc1ecc-ec18-415c-84f8-276ec581b24e">GetLength</a>
</td>
<td align="left" width="63%">
Gets the body length of the entitlement descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/484de26a-24e5-431d-ba4d-f2f3005502a1">GetTag</a>
</td>
<td align="left" width="63%">
Gets the tag that uniquely identifies the entitlement descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3fc73b0c-cacb-491b-b25b-49eb57154a37">GetToken</a>
</td>
<td align="left" width="63%">
Gets the entitlement token from the entitlement descriptor.

</td>
</tr>
</table> 

