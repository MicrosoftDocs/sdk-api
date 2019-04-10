---
UID: NN:mediaobj.IDMOQualityControl
title: IDMOQualityControl (mediaobj.h)
author: windows-sdk-content
description: The IDMOQualityControl interface supports quality control on a Microsoft DirectX Media Object (DMO).
old-location: dshow\idmoqualitycontrol.htm
tech.root: DirectShow
ms.assetid: c23211f2-d4ba-45ff-b443-3425c3a3e72f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDMOQualityControl, IDMOQualityControl interface [DirectShow], IDMOQualityControl interface [DirectShow],described, IDMOQualityControlInterface, dshow.idmoqualitycontrol, mediaobj/IDMOQualityControl
ms.topic: interface
req.header: mediaobj.h
req.include-header: Dmoguids.lib
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
 - Mediaobj.h
api_name:
 - IDMOQualityControl
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDMOQualityControl interface


## -description



The <code>IDMOQualityControl</code> interface supports quality control on a Microsoft DirectX Media Object (DMO).



A DMO exposes this interface if it can respond to late samples. When quality control is enabled, the DMO attempts to process samples on time, discarding late samples if necessary. When quality control is disabled, the DMO processes every sample. By default, quality control is disabled.

Applications use this interface to enable or disable quality control. Using quality control is appropriate when you are viewing media data in real time. If you are capturing data to a file, do not enable quality control, because the DMO might discard samples. It does not matter in file capture whether samples arrive late, and you do not want to lose the data.

To use quality control, perform the following steps:
<ol>
<li>Call the <a href="https://msdn.microsoft.com/en-us/library/Dd406841(v=VS.85).aspx">IDMOQualityControl::SetNow</a> method with the reference time of the earliest sample to be processed.</li>
<li>Call the <a href="https://msdn.microsoft.com/en-us/library/Dd406842(v=VS.85).aspx">IDMOQualityControl::SetStatus</a> method with the DMO_QUALITY_STATUS_ENABLED flag.</li>
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
<a href="https://msdn.microsoft.com/en-us/library/Dd406840(v=VS.85).aspx">GetStatus</a>
</td>
<td align="left" width="63%">
Determines whether quality control is active.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd406841(v=VS.85).aspx">SetNow</a>
</td>
<td align="left" width="63%">
Specifies the earliest time stamp for which the DMO should deliver data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd406842(v=VS.85).aspx">SetStatus</a>
</td>
<td align="left" width="63%">
Enables or disables quality control.

</td>
</tr>
</table> 

