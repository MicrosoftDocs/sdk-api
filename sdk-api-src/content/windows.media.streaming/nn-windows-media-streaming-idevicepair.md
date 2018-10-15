---
UID: NN:windows.media.streaming.IDevicePair
title: IDevicePair
author: windows-sdk-content
description: Represents a pair of ActiveBasicDevice objects which is comprised of a renderer and a server.
old-location: mediastreaming\idevicepair.htm
tech.root: mediastreaming
ms.assetid: 0129ABDA-E634-4236-A3A9-76C94D35D052
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: IDevicePair, IDevicePair interface [Media Streaming API], IDevicePair interface [Media Streaming API],described, mediastreaming.idevicepair, windows/IDevicePair
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
---

# IDevicePair interface


## -description


Represents a pair of <a href="https://msdn.microsoft.com/B747505A-7F8F-44F4-A9B3-73A8FE424D5F">ActiveBasicDevice</a> objects which is comprised of a renderer and a server.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDevicePair</b> interface inherits from <a href="https://msdn.microsoft.com/0657E51F-D4C0-46C6-927D-B01E54B6846C">IInspectable</a>. <b>IDevicePair</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/A130AB29-285A-4BBB-B02F-8DA515E0E529">Renderer</a>
</td>
<td align="left" width="63%">
Gets the renderer for the active basic device pair.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/F362617D-E0F8-4F2C-8968-93AD25FE0990">Server</a>
</td>
<td align="left" width="63%">
Gets the server for the active basic device pair.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/B747505A-7F8F-44F4-A9B3-73A8FE424D5F">ActiveBasicDevice</a>



<a href="https://msdn.microsoft.com/89A080E7-593B-406F-9E9B-4EC5838A619E">BasicDevice</a>



<a href="https://msdn.microsoft.com/0657E51F-D4C0-46C6-927D-B01E54B6846C">IInspectable</a>
 

 

