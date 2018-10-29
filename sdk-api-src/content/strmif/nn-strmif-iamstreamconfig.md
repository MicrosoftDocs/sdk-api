---
UID: NN:strmif.IAMStreamConfig
title: IAMStreamConfig
author: windows-sdk-content
description: The IAMStreamConfig interface sets the output format on certain capture and compression filters, for both audio and video.
old-location: dshow\iamstreamconfig.htm
tech.root: DirectShow
ms.assetid: c171763e-9108-49a0-a4b7-855c6db0a71d
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: IAMStreamConfig, IAMStreamConfig interface [DirectShow], IAMStreamConfig interface [DirectShow],described, IAMStreamConfigInterface, dshow.iamstreamconfig, strmif/IAMStreamConfig
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IAMStreamConfig
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAMStreamConfig interface


## -description


The <b>IAMStreamConfig</b> interface sets the output format on certain capture and compression filters, for both audio and video. Applications can use this interface to set format properties, such as the output dimensions and frame rate (for video) or the sample rate and number of channels (for audio).


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAMStreamConfig</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAMStreamConfig</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAMStreamConfig</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5443141b-eb2c-412c-8bd1-7175e724b602">GetFormat</a>
</td>
<td align="left" width="63%">
Retrieves the current or preferred output format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/355b8c4c-6d07-4d31-8dc5-ddc5ec2bf1cd">GetNumberOfCapabilities</a>
</td>
<td align="left" width="63%">
Retrieves the number of format capabilities that this pin supports.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9dd84847-2cae-42f2-a858-7106cd2ac075">GetStreamCaps</a>
</td>
<td align="left" width="63%">
Retrieves a set of format capabilities.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8d64e5b6-e8fa-4678-92d4-3cbf92e13ddf">SetFormat</a>
</td>
<td align="left" width="63%">
Sets the output format on the pin.

</td>
</tr>
</table> 


## -remarks



Filters expose this interface on their output pins. To use the interface, enumerate the filter's pins and query for <b>IAMStreamConfig</b>. Or, if you are using the <a href="https://msdn.microsoft.com/df59afcf-6e11-463f-80ac-8b1fcc496d5b">Capture Graph Builder</a> object to build the filter graph, you can call the <a href="https://msdn.microsoft.com/931b42bf-25d6-4f0a-8c45-baf8ed65e302">ICaptureGraphBuilder2::FindInterface</a> method. Note that a capture filter might have separate pins for capture and preview.

<h3><a id="Filter_Developers"></a><a id="filter_developers"></a><a id="FILTER_DEVELOPERS"></a>Filter Developers</h3>
If you are writing a capture filter or compression filter, implement this interface on the video or audio output pin. For more information, see <a href="https://msdn.microsoft.com/f7466cfe-b13e-4ee9-82f9-0528ed97bf99">Exposing Capture and Compression Formats</a>.




## -see-also




<a href="https://msdn.microsoft.com/5efd174f-2eb1-44e6-97e3-b73c7c52fef1">Interfaces</a>
 

 

