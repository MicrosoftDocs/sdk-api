---
UID: NN:wmcodecdsp.IWMVideoDecoderHurryup
title: IWMVideoDecoderHurryup
author: windows-sdk-content
description: Controls the speed of the video decoder.
old-location: mf\iwmvideodecoderhurryupinterface.htm
old-project: medfound
ms.assetid: 5e33be5f-5ce8-4f4f-94db-4be2dfcaeec0
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: IWMVideoDecoderHurryup, IWMVideoDecoderHurryup interface [Media Foundation], IWMVideoDecoderHurryup interface [Media Foundation],described, codecapi.iwmvideodecoderhurryupinterface, mf.iwmvideodecoderhurryup, mf.iwmvideodecoderhurryupinterface, wmcodecdsp/IWMVideoDecoderHurryup
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
 - IWMVideoDecoderHurryup
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmvdspa.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMVideoDecoderHurryup interface


## -description



Controls the speed of the video decoder.



This interface is implemented by the video decoder objects. You can obtain a pointer to <a href="mf.iwmvideodecoderhurryup">IWMVideoDecoderHurryup</a> by calling the <b>QueryInterface</b> method of any other interface of the decoder, such as <a href="https://msdn.microsoft.com/a3fd17aa-7df2-40f4-8f2c-45bae38e4c0b">IMediaObject</a> or <a href="https://msdn.microsoft.com/3cc502d8-d364-43b9-b0b6-d9474c002b20">IMFTransform</a>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMVideoDecoderHurryup</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWMVideoDecoderHurryup</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMVideoDecoderHurryup</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c5c58acd-ebf9-46ce-977b-1478b42559c4">GetHurryup</a>
</td>
<td align="left" width="63%">
Retrieves the current speed mode of the video decoder.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ef01d2ab-2525-4caf-87d9-3acdc0b3b1b3">SetHurryup</a>
</td>
<td align="left" width="63%">
Sets the speed mode of the video decoder.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>
 

 

