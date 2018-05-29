---
UID: NN:dvbsiparser.IPBDAAttributesDescriptor
title: IPBDAAttributesDescriptor
author: windows-sdk-content
description: Implements methods that get data from anattributes descriptor in a Protected Broadcast Device Architecture (PBDA) transport stream.
old-location: mstv\ipbdaattributesdescriptor.htm
old-project: mstv
ms.assetid: 489348b7-0f10-4a49-a7d4-10a1ed478aa8
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IPBDAAttributesDescriptor, IPBDAAttributesDescriptor interface [Microsoft TV Technologies], IPBDAAttributesDescriptor interface [Microsoft TV Technologies],described, dvbsiparser/IPBDAAttributesDescriptor, mstv.ipbdaattributesdescriptor
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
req.typenames: DSROLE_UPGRADE_STATUS_INFO, *PDSROLE_UPGRADE_STATUS_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	dvbsiparser.h
api_name:
-	IPBDAAttributesDescriptor
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IPBDAAttributesDescriptor interface


## -description


Implements methods that get data from anattributes descriptor in a Protected Broadcast  Device Architecture (PBDA) transport stream.

For more information about PBDA, download the specification from <a href="http://go.microsoft.com/fwlink/p/?linkid=132926">http://go.microsoft.com/fwlink/p/?linkid=132926</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPBDAAttributesDescriptor</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IPBDAAttributesDescriptor</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/315f6afe-a5cc-4fe2-8029-fcf280b358b2">GetAttributePayload</a>
</td>
<td align="left" width="63%">
Gets the descriptor body from the attributes descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b18ebaa1-aca4-4d21-adb7-d233e18cd320">GetLength</a>
</td>
<td align="left" width="63%">
Gets the body length of the  attributes descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/397e76b6-83f2-4d0c-87a0-0575aa746020">GetTag</a>
</td>
<td align="left" width="63%">
Gets the tag that uniquely identifies the attributes descriptor.

</td>
</tr>
</table> 

