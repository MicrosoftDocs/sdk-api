---
UID: NN:mfidl.IMFQualityAdvise
title: IMFQualityAdvise (mfidl.h)
description: Enables the quality manager to adjust the audio or video quality of a component in the pipeline.
helpviewer_keywords: ["20681ce7-e07e-4e34-9238-ec23cc6bfc84","IMFQualityAdvise","IMFQualityAdvise interface [Media Foundation]","IMFQualityAdvise interface [Media Foundation]","described","mf.imfqualityadvise","mfidl/IMFQualityAdvise"]
old-location: mf\imfqualityadvise.htm
tech.root: medfound
ms.assetid: 20681ce7-e07e-4e34-9238-ec23cc6bfc84
ms.date: 12/05/2018
ms.keywords: 20681ce7-e07e-4e34-9238-ec23cc6bfc84, IMFQualityAdvise, IMFQualityAdvise interface [Media Foundation], IMFQualityAdvise interface [Media Foundation],described, mf.imfqualityadvise, mfidl/IMFQualityAdvise
f1_keywords:
- mfidl/IMFQualityAdvise
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFQualityAdvise interface


## -description


Enables the quality manager to adjust the audio or video quality of a component in the pipeline.

This interface is exposed by pipeline components that can adjust their quality. Typically it is exposed by decoders and stream sinks. For example, the enhanced video renderer (EVR) implements this interface. However, media sources can also implement this interface.

To get a pointer to this interface from a media source, call <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice">IMFGetService::GetService</a> with the service identifier MF_QUALITY_SERVICES. For all other pipeline objects (transforms and media sinks), call <b>QueryInterface</b>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFQualityAdvise</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFQualityAdvise</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfqualityadvise-droptime">DropTime</a>
</td>
<td align="left" width="63%">
Drops samples over a specified interval of time.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfqualityadvise-getdropmode">GetDropMode</a>
</td>
<td align="left" width="63%">
Retrieves the current drop mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfqualityadvise-getqualitylevel">GetQualityLevel</a>
</td>
<td align="left" width="63%">
Retrieves the current quality level.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfqualityadvise-setdropmode">SetDropMode</a>
</td>
<td align="left" width="63%">
Sets the drop mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfqualityadvise-setqualitylevel">SetQualityLevel</a>
</td>
<td align="left" width="63%">
Sets the quality level.

</td>
</tr>
</table> 


## -remarks



The quality manager typically obtains this interface when the quality manager's <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfqualitymanager-notifytopology">IMFQualityManager::NotifyTopology</a> method is called.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfqualitymanager">IMFQualityManager</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
 

 

