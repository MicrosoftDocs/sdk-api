---
UID: NN:mfidl.IMFVideoProcessorControl
title: IMFVideoProcessorControl
author: windows-sdk-content
description: Configures the Video Processor MFT.
old-location: mf\imfvideoprocessorcontrol.htm
old-project: medfound
ms.assetid: 6803B69E-CF84-45D5-804C-BD961BD5E13D
ms.author: windowssdkdev
ms.date: 06/05/2018
ms.keywords: IMFVideoProcessorControl, IMFVideoProcessorControl interface [Media Foundation], IMFVideoProcessorControl interface [Media Foundation],described, mf.imfvideoprocessorcontrol, mfidl/IMFVideoProcessorControl
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps | UWP apps]
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
req.typenames: MFSensorDeviceMode
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
req.lib: Mfuuid.lib
req.dll: Mfsensorgroup.dll
req.irql: 
req.product: GDI+ 1.1
---

# IMFVideoProcessorControl interface


## -description


Configures the <a href="https://msdn.microsoft.com/1476995A-9692-4B08-8EF7-7DB6321BEC24">Video Processor MFT</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFVideoProcessorControl</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFVideoProcessorControl</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/DA6165C9-24E9-473C-A4F7-4C94399AF346">SetBorderColor</a>
</td>
<td align="left" width="63%">
Sets the border color.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/876F8BA0-9F05-48C6-ADE9-D65E7682C545">SetConstrictionSize</a>
</td>
<td align="left" width="63%">
Specifies the amount of downsampling to perform on the output.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8AD1BDF4-2508-4A99-85A1-9DBC969D511B">SetDestinationRectangle</a>
</td>
<td align="left" width="63%">
Sets the destination rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4529FEE5-7FDF-4EFF-93C1-E20A63186496">SetMirror</a>
</td>
<td align="left" width="63%">
Specifies whether to flip the video image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/452FE057-EC1A-430E-A5C8-C9B84A4B1B17">SetRotation</a>
</td>
<td align="left" width="63%">
Specifies whether to rotate the video to the correct orientation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0A4E74BB-6F98-4610-9F47-5BD1E58B8589">SetSourceRectangle</a>
</td>
<td align="left" width="63%">
Sets the source rectangle.

</td>
</tr>
</table> 


## -remarks



This interface controls how the <a href="https://msdn.microsoft.com/1476995A-9692-4B08-8EF7-7DB6321BEC24">Video Processor MFT</a> generates output frames.




## -see-also




<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>
 

 

