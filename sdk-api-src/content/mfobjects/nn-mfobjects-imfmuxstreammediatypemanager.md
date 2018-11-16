---
UID: NN:mfobjects.IMFMuxStreamMediaTypeManager
title: IMFMuxStreamMediaTypeManager
author: windows-sdk-content
description: Enables the management of stream configurations for a multiplexed media source. A stream configuration defines a set of substreams that can be included the multiplexed output.
old-location: mf\imfmuxstreammediatypemanager.htm
tech.root: medfound
ms.assetid: BBDAEF1C-DFEC-4647-8B74-E2ABB25F87CC
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IMFMuxStreamMediaTypeManager, IMFMuxStreamMediaTypeManager interface [Media Foundation], IMFMuxStreamMediaTypeManager interface [Media Foundation],described, mf.imfmuxstreammediatypemanager, mfobjects/IMFMuxStreamMediaTypeManager
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: mfobjects.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1703 [desktop apps only]
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
req.lib: Mfplat.lib; Mfplat.dll
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfplat.lib
 - mfplat.dll
 - mfplat.dll
 - mfplat.dll.dll
api_name:
 - IMFMuxStreamMediaTypeManager
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFMuxStreamMediaTypeManager interface


## -description


Enables the management of stream configurations for a multiplexed media source. A stream configuration defines a set of substreams that can be included  the  multiplexed output.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFMuxStreamMediaTypeManager</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFMuxStreamMediaTypeManager</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFMuxStreamMediaTypeManager</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9A647B60-ACA0-4878-A75B-54CA093DEDD0">AddStreamConfiguration</a>
</td>
<td align="left" width="63%">
Registers a stream configuration, which defines a set of substreams that can be included  the  multiplexed output.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1C00900F-BD8B-4AF7-82E0-37AC370A90E3">GetAttributes</a>
</td>
<td align="left" width="63%">
Gets the <a href="https://msdn.microsoft.com/e12259f4-b631-4d4a-a296-c1cc6334b962">IMFAttributes</a> for the substream with the specified index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/F8A65783-7FD8-46C2-87B0-BC540E1F187F">GetMediaType</a>
</td>
<td align="left" width="63%">
Gets the <a href="https://msdn.microsoft.com/f1d60bec-71e4-4fcc-a020-92754b6f3c02">IMFMediaType</a> of the substream with the specified index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5B2B7F8C-0D3B-4BBB-8445-1A428A29A272">GetStreamConfiguration</a>
</td>
<td align="left" width="63%">
Gets the stream configuration with the specified index, which defines a set of substreams that can be included  the  multiplexed output.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9591BFEC-DD25-41A8-9DA8-7F39158CB442">GetStreamConfigurationCount</a>
</td>
<td align="left" width="63%">
Gets the count of registered stream configurations, which define set of substreams that can be included  the  multiplexed output.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/631802B5-00F7-4219-9B21-5A1FB8628477">GetStreamCount</a>
</td>
<td align="left" width="63%">
Gets the count of substreams managed by the multiplexed media source.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/EEEF5D71-22C4-4050-9088-8BAC554EB66E">GetStreamCount</a>
</td>
<td align="left" width="63%">
Gets the count of substreams managed by the multiplexed media source.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8808DC0A-7675-4913-B4F1-B2FCCB3AFBBF">RemoveStreamConfiguration</a>
</td>
<td align="left" width="63%">
Unregisters a stream configuration, which defines a set of substreams that can be included  the  multiplexed output.

</td>
</tr>
</table> 

