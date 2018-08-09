---
UID: NN:wmcodecdsp.IWMCodecLeakyBucket
title: IWMCodecLeakyBucket
author: windows-sdk-content
description: Configures the &#0034;leaky bucket&#0034; parameters on a video encoder.
old-location: mf\iwmcodecleakybucketinterface.htm
old-project: medfound
ms.assetid: 93a0169e-39fe-4152-8698-72a0650be41a
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: IWMCodecLeakyBucket, IWMCodecLeakyBucket interface [Media Foundation], IWMCodecLeakyBucket interface [Media Foundation],described, codecapi.iwmcodecleakybucketinterface, mf.iwmcodecleakybucketinterface, wmcodecdsp/IWMCodecLeakyBucket
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: wmcodecdsp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: MFVideoDSPMode
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmcodecdsp.h
api_name:
 - IWMCodecLeakyBucket
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmvdspa.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMCodecLeakyBucket interface


## -description


Configures the "leaky bucket" parameters on a video encoder.

This interface is implemented by all of the encoder objects. You can get a pointer to the <b>IWMCodecLeakyBucket</b> interface for a Windows Media video encoder by calling the <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> method of any other interface on the object, such as <a href="https://msdn.microsoft.com/a3fd17aa-7df2-40f4-8f2c-45bae38e4c0b">IMediaObject</a> or <a href="https://msdn.microsoft.com/3cc502d8-d364-43b9-b0b6-d9474c002b20">IMFTransform</a>. This interface is not  implemented on any of the decoders.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMCodecLeakyBucket</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWMCodecLeakyBucket</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMCodecLeakyBucket</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/46eee8c9-e10e-41e3-9400-051b4484eee0">GetBufferFullnessBits</a>
</td>
<td align="left" width="63%">
Not implemented in this release.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7fa0835e-7386-4032-a94b-ef52259aeea9">GetBufferSizeBits</a>
</td>
<td align="left" width="63%">
Retrieves the  current size of the buffer in bits.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e82badb3-64a8-40f0-9c51-bb2539f242f2">SetBufferFullnessBits</a>
</td>
<td align="left" width="63%">
Not  implemented in this release.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b602e8ca-8446-4f94-bcd0-193084d96565">SetBufferSizeBits</a>
</td>
<td align="left" width="63%">
Sets the buffer size in bits.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>



<a href="https://msdn.microsoft.com/2f7f80d6-3abb-462f-a571-b223a1d59da6">The Leaky Bucket Buffer Model</a>
 

 

