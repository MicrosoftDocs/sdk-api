---
UID: NN:windows.media.streaming.IDevicePair
title: IDevicePair (windows.media.streaming.h)
author: windows-sdk-content
description: Represents a pair of ActiveBasicDevice objects which is comprised of a renderer and a server.
old-location: mediastreaming\idevicepair.htm
tech.root: mediastreaming
ms.assetid: 0129ABDA-E634-4236-A3A9-76C94D35D052
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDevicePair, IDevicePair interface [Media Streaming API], IDevicePair interface [Media Streaming API],described, mediastreaming.idevicepair, windows/IDevicePair
ms.topic: interface
f1_keywords: ["windows.media.streaming/IDevicePair"]
req.header: windows.media.streaming.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Windows.Media.Streaming.Devices.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: PlayToDevice.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - PlayToDevice.dll
api_name:
 - IDevicePair
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDevicePair interface


## -description


Represents a pair of <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/dn385755(v=vs.85)">ActiveBasicDevice</a> objects which is comprised of a renderer and a server.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDevicePair</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/inspectable/nn-inspectable-iinspectable">IInspectable</a>. <b>IDevicePair</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDevicePair</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-idevicepair-get_renderer">Renderer</a>
</td>
<td align="left" width="63%">
Gets the renderer for the active basic device pair.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-idevicepair-get_server">Server</a>
</td>
<td align="left" width="63%">
Gets the server for the active basic device pair.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/dn385755(v=vs.85)">ActiveBasicDevice</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh828813(v=vs.85)">BasicDevice</a>



<a href="https://docs.microsoft.com/windows/desktop/api/inspectable/nn-inspectable-iinspectable">IInspectable</a>
 

 

