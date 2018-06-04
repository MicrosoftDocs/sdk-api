---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# IDMOQualityControl interface


## -description



The <code>IDMOQualityControl</code> interface supports quality control on a Microsoft DirectX Media Object (DMO).



A DMO exposes this interface if it can respond to late samples. When quality control is enabled, the DMO attempts to process samples on time, discarding late samples if necessary. When quality control is disabled, the DMO processes every sample. By default, quality control is disabled.

Applications use this interface to enable or disable quality control. Using quality control is appropriate when you are viewing media data in real time. If you are capturing data to a file, do not enable quality control, because the DMO might discard samples. It does not matter in file capture whether samples arrive late, and you do not want to lose the data.

To use quality control, perform the following steps:
<ol>
<li>Call the <a href="https://msdn.microsoft.com/36efee4f-0a06-421f-bc37-688a6499bda7">IDMOQualityControl::SetNow</a> method with the reference time of the earliest sample to be processed.</li>
<li>Call the <a href="https://msdn.microsoft.com/d22a7a23-6623-4a98-9a0c-5195b29781f9">IDMOQualityControl::SetStatus</a> method with the DMO_QUALITY_STATUS_ENABLED flag.</li>
</ol>To disable quality control, call <b>SetStatus</b> with no flag.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDMOQualityControl</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDMOQualityControl</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDMOQualityControl</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh406321">GetStatus</a>
</td>
<td align="left" width="63%">
Determines whether quality control is active.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/36efee4f-0a06-421f-bc37-688a6499bda7">SetNow</a>
</td>
<td align="left" width="63%">
Specifies the earliest time stamp for which the DMO should deliver data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d22a7a23-6623-4a98-9a0c-5195b29781f9">SetStatus</a>
</td>
<td align="left" width="63%">
Enables or disables quality control.

</td>
</tr>
</table> 

