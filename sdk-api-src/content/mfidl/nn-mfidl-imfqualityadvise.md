---
UID: NN:mfidl.IMFQualityAdvise
title: IMFQualityAdvise
author: windows-sdk-content
description: Enables the quality manager to adjust the audio or video quality of a component in the pipeline.
old-location: mf\imfqualityadvise.htm
tech.root: medfound
ms.assetid: 20681ce7-e07e-4e34-9238-ec23cc6bfc84
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: 20681ce7-e07e-4e34-9238-ec23cc6bfc84, IMFQualityAdvise, IMFQualityAdvise interface [Media Foundation], IMFQualityAdvise interface [Media Foundation],described, mf.imfqualityadvise, mfidl/IMFQualityAdvise
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFQualityAdvise
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFQualityAdvise interface


## -description


Enables the quality manager to adjust the audio or video quality of a component in the pipeline.

This interface is exposed by pipeline components that can adjust their quality. Typically it is exposed by decoders and stream sinks. For example, the enhanced video renderer (EVR) implements this interface. However, media sources can also implement this interface.

To get a pointer to this interface from a media source, call <a href="https://msdn.microsoft.com/4287dd1f-1718-4231-bc62-b58e0e61d688">IMFGetService::GetService</a> with the service identifier MF_QUALITY_SERVICES. For all other pipeline objects (transforms and media sinks), call <b>QueryInterface</b>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFQualityAdvise</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFQualityAdvise</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFQualityAdvise</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/60d27190-7bed-427c-9018-2926c85815fe">DropTime</a>
</td>
<td align="left" width="63%">
Drops samples over a specified interval of time.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bb700a3e-837f-4e88-a9b7-294c41143402">GetDropMode</a>
</td>
<td align="left" width="63%">
Retrieves the current drop mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9a2b501e-543d-4ba0-86a1-a55e7d136685">GetQualityLevel</a>
</td>
<td align="left" width="63%">
Retrieves the current quality level.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/190de66a-6c47-49d5-a8f6-c2fb57a7aee2">SetDropMode</a>
</td>
<td align="left" width="63%">
Sets the drop mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f788fd7d-65fc-4917-8d5d-cfaf35a013e7">SetQualityLevel</a>
</td>
<td align="left" width="63%">
Sets the quality level.

</td>
</tr>
</table> 


## -remarks



The quality manager typically obtains this interface when the quality manager's <a href="https://msdn.microsoft.com/5ff6d923-4a83-401a-a0de-0b1a732c31a5">IMFQualityManager::NotifyTopology</a> method is called.




## -see-also




<a href="https://msdn.microsoft.com/66781a1f-7469-4222-9e99-6b1415830f4c">IMFQualityManager</a>



<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>
 

 

