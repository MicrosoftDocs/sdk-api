---
UID: NN:tuner.IMPEG2Component
title: IMPEG2Component
author: windows-driver-content
description: The IMPEG2Component interface contains methods for getting and setting properties that describe an MPEG2 elementary stream.
old-location: mstv\impeg2component.htm
old-project: mstv
ms.assetid: 63d1ae17-8e38-457e-98d7-e81e7576f1c1
ms.author: windowsdriverdev
ms.date: 5/14/2018
ms.keywords: IMPEG2Component, IMPEG2Component interface [Microsoft TV Technologies], IMPEG2Component interface [Microsoft TV Technologies],described, IMPEG2ComponentInterface, mstv.impeg2component, tuner/IMPEG2Component
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: tuner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Tuner.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: BITMAP_RENDERER_STATISTICS, *PBITMAP_RENDERER_STATISTICS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	tuner.h
api_name:
-	IMPEG2Component
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IMPEG2Component interface


## -description



The <b>IMPEG2Component</b> interface contains methods for getting and setting properties that describe an MPEG2 elementary stream. These properties are set by the TIF or Guide Store loader based on data in the transport stream tables. After the tune request is retrieved from the Guide Store and submitted either to the Video Control or directly to the Network Provider, these properties are used by the Network Provider and MPEG-2 Demultiplexer to acquire the specified substream and pass it to the downstream filters.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMPEG2Component</b> interface inherits from <a href="https://msdn.microsoft.com/516b30ba-4f55-49b7-8085-d436bf4a94e1">IComponent</a>. <b>IMPEG2Component</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMPEG2Component</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b31f04b6-e2b1-450b-9f1f-2df0c9055da2">get_PCRPID</a>
</td>
<td align="left" width="63%">
Returns the MPEG2 Packet ID (PID) for this substream's time stamps.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7d6b0b2f-fe48-4fc5-bb3b-639bb8ee2df8">get_PID</a>
</td>
<td align="left" width="63%">
Get the packet identifier for this substream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a501c65d-26cf-44f4-b134-2a1080095eaa">get_ProgramNumber</a>
</td>
<td align="left" width="63%">
Gets the program number, which provides a reverse lookup to PAT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cfe55ec9-cf07-40c5-98da-cb23393490d0">put_PCRPID</a>
</td>
<td align="left" width="63%">
Sets the MPEG2 Packet ID for this substream's time stamps.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0bc19b79-1586-470d-85d5-3ef1babe60e2">put_PID</a>
</td>
<td align="left" width="63%">
Set the packet identifier for this substream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f8bc605f-6e3f-427c-a91e-2d4cbb59b65e">put_ProgramNumber</a>
</td>
<td align="left" width="63%">
Sets the program number, which provides a reverse lookup to PAT.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IMPEG2Component)</code>.




## -see-also




<a href="https://msdn.microsoft.com/516b30ba-4f55-49b7-8085-d436bf4a94e1">IComponent</a>



<a href="https://msdn.microsoft.com/5d956e1d-88b3-4236-9987-f37f674645de">Tuning Model Interfaces</a>
 

 

