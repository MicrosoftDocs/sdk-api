---
UID: NN:mfidl.IMFVideoProcessorControl2
title: IMFVideoProcessorControl2
author: windows-sdk-content
description: Configures the Video Processor MFT.
old-location: mf\imfvideoprocessorcontrol2.htm
old-project: medfound
ms.assetid: FE314254-AAE4-482E-A7AE-28B2591E0060
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: IMFVideoProcessorControl2, IMFVideoProcessorControl2 interface [Media Foundation], IMFVideoProcessorControl2 interface [Media Foundation],described, mf.imfvideoprocessorcontrol2, mfidl/IMFVideoProcessorControl2
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: mfidl.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2016 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mfidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: MFSensorDeviceMode
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfidl.h
api_name:
 - IMFVideoProcessorControl2
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: Mfsensorgroup.dll
req.irql: 
req.product: GDI+ 1.1
---

# IMFVideoProcessorControl2 interface


## -description


Configures the <a href="https://msdn.microsoft.com/1476995A-9692-4B08-8EF7-7DB6321BEC24">Video Processor MFT</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFVideoProcessorControl2</b> interface inherits from <a href="https://msdn.microsoft.com/6803B69E-CF84-45D5-804C-BD961BD5E13D">IMFVideoProcessorControl</a>. <b>IMFVideoProcessorControl2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFVideoProcessorControl2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/682B1FAA-05D5-40E3-98BD-DDEFB0C5B4AF">EnableHardwareEffects</a>
</td>
<td align="left" width="63%">
Enables effects that were implemented with <a href="https://msdn.microsoft.com/D526BB31-A4B9-4BBD-BAE3-43FDFF58A32A">IDirectXVideoProcessor::VideoProcessorBlt</a>. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0D5FE2B8-B8DD-40DE-8B41-40E773976BE6">GetSupportedHardwareEffects</a>
</td>
<td align="left" width="63%">
Returns the list of supported effects in the currently configured video processor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/408048CF-0443-4F09-8AB9-A9A2827EA749">SetRotationOverride</a>
</td>
<td align="left" width="63%">
Overrides the rotation operation that is performed in the video processor.

</td>
</tr>
</table> 


## -remarks



This interface controls how the <a href="https://msdn.microsoft.com/1476995A-9692-4B08-8EF7-7DB6321BEC24">Video Processor MFT</a> generates output frames.




## -see-also




<a href="https://msdn.microsoft.com/6803B69E-CF84-45D5-804C-BD961BD5E13D">IMFVideoProcessorControl</a>



<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>
 

 

