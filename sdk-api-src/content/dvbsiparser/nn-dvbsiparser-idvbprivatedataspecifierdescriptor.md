---
UID: NN:dvbsiparser.IDvbPrivateDataSpecifierDescriptor
title: IDvbPrivateDataSpecifierDescriptor
author: windows-sdk-content
description: Implements methods that get data from a Digital Video Broadcast (DVB) private data descriptor. The private data descriptor describes broadcaster-specific data that is not part of the official MPEG-2 standard for broadcast streams.
old-location: mstv\idvbprivatedataspecifierdescriptor.htm
old-project: mstv
ms.assetid: 0d5a78a3-0d56-47e8-939f-006d5f4db5c4
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IDvbPrivateDataSpecifierDescriptor, IDvbPrivateDataSpecifierDescriptor interface [Microsoft TV Technologies], IDvbPrivateDataSpecifierDescriptor interface [Microsoft TV Technologies],described, dvbsiparser/IDvbPrivateDataSpecifierDescriptor, mstv.idvbprivatedataspecifierdescriptor
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: dvbsiparser.h
req.include-header: Dvbsiparser.idl
req.redist: 
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
 - IDvbPrivateDataSpecifierDescriptor
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDvbPrivateDataSpecifierDescriptor interface


## -description


Implements methods that get data from a Digital Video Broadcast (DVB) private data descriptor. The private data descriptor describes broadcaster-specific data that is not part of the official MPEG-2 standard for broadcast streams.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDvbPrivateDataSpecifierDescriptor</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDvbPrivateDataSpecifierDescriptor</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDvbPrivateDataSpecifierDescriptor</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9a3b550c-3082-4ac8-9568-6ccdec26d193">GetLength</a>
</td>
<td align="left" width="63%">
Gets the body length of a DVB private data descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bb5b7d8a-6699-49b4-8935-8bfd07d85290">GetPrivateDataSpecifier</a>
</td>
<td align="left" width="63%">
Gets data from a DVB private data descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bccca68c-d480-47d0-a0db-7a7d3f8376c2">GetTag</a>
</td>
<td align="left" width="63%">
Gets the tag that identifies a DVB private data descriptor.

</td>
</tr>
</table> 

