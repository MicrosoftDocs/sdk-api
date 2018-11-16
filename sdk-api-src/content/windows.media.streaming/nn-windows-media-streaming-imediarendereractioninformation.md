---
UID: NN:windows.media.streaming.IMediaRendererActionInformation
title: IMediaRendererActionInformation
author: windows-sdk-content
description: Encapsulates the methods needed to provide information about what methods can currently be invoked on the DMR.
old-location: mediastreaming\imediarendereractioninformation.htm
tech.root: mediastreaming
ms.assetid: 854C7024-D582-405D-8A5F-C152DE8BE0BE
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IMediaRendererActionInformation, IMediaRendererActionInformation interface [Media Streaming API], IMediaRendererActionInformation interface [Media Streaming API],described, mediastreaming.imediarendereractioninformation, windows/IMediaRendererActionInformation
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: windows.media.streaming.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - windows.media.streaming.h
api_name:
 - IMediaRendererActionInformation
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMediaRendererActionInformation interface


## -description


Encapsulates the methods needed to provide information about what methods can currently be invoked on the DMR.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMediaRendererActionInformation</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMediaRendererActionInformation</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMediaRendererActionInformation</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/F744C2D7-5518-4A9F-A71E-60CF0B312177">IsMuteAvailable</a>
</td>
<td align="left" width="63%">
Retrieves a value that indicates whether the DMR is capable of muting the audio.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/095A664F-D974-410D-8741-87A171EDD071">IsPauseAvailable</a>
</td>
<td align="left" width="63%">
Retrieves a value that indicates whether the DMR is currently accepting the <a href="https://msdn.microsoft.com/2EADD9BE-2306-4CDA-AD5C-8342C06EAF1B">PauseAsync</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/969C55FA-872D-4063-B85C-573C8DA5593C">IsPlayAvailable</a>
</td>
<td align="left" width="63%">
Retrieves a value that indicates whether the DMR is currently accepting the accepting the <a href="https://msdn.microsoft.com/32084664-2D1B-4303-B3B7-9B896A07CB17">PlayAsync</a> and <a href="https://msdn.microsoft.com/368510CF-FC36-4D92-AE92-024D53EE3BAD">PlayAtSpeedAsync</a> methods.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/F0817184-70F2-43AC-A2BE-A15F4B195085">IsSeekAvailable</a>
</td>
<td align="left" width="63%">
Retrieves a value that indicates whether the DMR is currently accepting the <a href="https://msdn.microsoft.com/3179A942-7756-4763-A2F8-629D89D39542">SeekAsync</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7588E992-4070-4E0F-8C4B-7DFC097A5076">IsSetNextSourceAvailable</a>
</td>
<td align="left" width="63%">
Retrieves a value that indicates whether the DMR is currently accepting the <a href="https://msdn.microsoft.com/6894F1DF-63E2-4091-B61B-736D801E06EF">SetNextSourceFromUriAsync</a> method, the <a href="https://msdn.microsoft.com/602B4C9B-88A3-4D91-9330-FC02E62F723A">SetNextSourceFromStreamAsync</a> method or the <a href="https://msdn.microsoft.com/054203C8-766B-4448-A275-CA61C9D177AD">SetNextSourceFromMediaSourceAsync</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6EE8F56D-2A5A-49B0-A9B2-0A7EE57D03FD">IsStopAvailable</a>
</td>
<td align="left" width="63%">
Retrieves a value that indicates whether the DMR is currently accepting the <a href="https://msdn.microsoft.com/B6B0F3F2-E95E-4A58-9CBD-CF4CB24FDAD0">StopAsync</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6DFDC37A-3304-4CDB-9928-C113D2F64ED0">IsVolumeAvailable</a>
</td>
<td align="left" width="63%">
Retrieves a value that indicates whether the DMR is capable of adjusting the audio volume level.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0AB63E39-6A26-4199-9978-A10866A7C805">PlaySpeeds</a>
</td>
<td align="left" width="63%">
Retrieves the complete list of <a href="https://msdn.microsoft.com/29b58229-8236-4c93-a6b4-ed09d1aca9db">PlaySpeed</a> values that are accepted by the DMR.

</td>
</tr>
</table> 

