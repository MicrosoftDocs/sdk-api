---
UID: NN:segment.IMSVidFilePlayback2
title: IMSVidFilePlayback2
author: windows-sdk-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 or later.
old-location: mstv\imsvidfileplayback2.htm
tech.root: mstv
ms.assetid: 5779d5f8-74b1-4318-9fda-1dae3bf4a3f5
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IMSVidFilePlayback2, IMSVidFilePlayback2 interface [Microsoft TV Technologies], IMSVidFilePlayback2 interface [Microsoft TV Technologies],described, IMSVidFilePlayback2Interface, mstv.imsvidfileplayback2, segment/IMSVidFilePlayback2
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: segment.h
req.include-header: Msvidctl.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Segment.idl
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
 - segment.h
api_name:
 - IMSVidFilePlayback2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMSVidFilePlayback2 interface


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 or later.
        



The <b>IMSVidFilePlayback2</b> interface enables the client to specify a DirectShow source filter for playback. It is implemented by the <a href="https://msdn.microsoft.com/da8a1d86-b3a5-4488-8bbc-82dd09aeeaca">MSVidFilePlaybackDevice</a> object. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMSVidFilePlayback2</b> interface inherits from <a href="https://msdn.microsoft.com/d6afaf69-5c1b-4f7f-a3cf-51268d6bc2b5">IMSVidFilePlayback</a>. <b>IMSVidFilePlayback2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMSVidFilePlayback2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/257e93ec-fb26-45fb-b07b-4491dbf2528a">put___SourceFilter</a>
</td>
<td align="left" width="63%">
Sets the CLSID of a DirectShow source filter to use for this source.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ef536087-dd2b-417f-b139-916d930e3d25">put__SourceFilter</a>
</td>
<td align="left" width="63%">
Sets the CLSID of a DirectShow source filter to use for this source. The CLSID is specified as a string.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IMSVidFilePlayback2)</code>.




## -see-also




<a href="https://msdn.microsoft.com/d6afaf69-5c1b-4f7f-a3cf-51268d6bc2b5">IMSVidFilePlayback</a>



<a href="https://msdn.microsoft.com/bf6c3ce9-1e56-4109-93f1-5b313e6ca19b">Video Control Interfaces</a>
 

 

