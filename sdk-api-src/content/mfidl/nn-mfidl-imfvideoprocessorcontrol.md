---
UID: NN:mfidl.IMFVideoProcessorControl
title: IMFVideoProcessorControl (mfidl.h)
author: windows-sdk-content
description: Configures the Video Processor MFT.
old-location: mf\imfvideoprocessorcontrol.htm
tech.root: medfound
ms.assetid: 6803B69E-CF84-45D5-804C-BD961BD5E13D
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMFVideoProcessorControl, IMFVideoProcessorControl interface [Media Foundation], IMFVideoProcessorControl interface [Media Foundation],described, mf.imfvideoprocessorcontrol, mfidl/IMFVideoProcessorControl
ms.topic: interface
f1_keywords: ["mfidl/IMFVideoProcessorControl"]
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
 - mfidl.h
api_name:
 - IMFVideoProcessorControl
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFVideoProcessorControl interface


## -description


Configures the <a href="https://docs.microsoft.com/windows/desktop/medfound/video-processor-mft">Video Processor MFT</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFVideoProcessorControl</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFVideoProcessorControl</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFVideoProcessorControl</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfvideoprocessorcontrol-setbordercolor">SetBorderColor</a>
</td>
<td align="left" width="63%">
Sets the border color.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfvideoprocessorcontrol-setconstrictionsize">SetConstrictionSize</a>
</td>
<td align="left" width="63%">
Specifies the amount of downsampling to perform on the output.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfvideoprocessorcontrol-setdestinationrectangle">SetDestinationRectangle</a>
</td>
<td align="left" width="63%">
Sets the destination rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfvideoprocessorcontrol-setmirror">SetMirror</a>
</td>
<td align="left" width="63%">
Specifies whether to flip the video image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfvideoprocessorcontrol-setrotation">SetRotation</a>
</td>
<td align="left" width="63%">
Specifies whether to rotate the video to the correct orientation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfvideoprocessorcontrol-setsourcerectangle">SetSourceRectangle</a>
</td>
<td align="left" width="63%">
Sets the source rectangle.

</td>
</tr>
</table> 


## -remarks



This interface controls how the <a href="https://docs.microsoft.com/windows/desktop/medfound/video-processor-mft">Video Processor MFT</a> generates output frames.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
 

 

