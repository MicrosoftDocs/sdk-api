---
UID: NN:mfmediaengine.IMFMediaEngineOPMInfo
title: IMFMediaEngineOPMInfo (mfmediaengine.h)
author: windows-sdk-content
description: Provides methods for getting information about the Output Protection Manager (OPM).
old-location: mf\imfmediaengineopminfo.htm
tech.root: medfound
ms.assetid: 399f81ac-38f8-4aaa-8b34-f5fd13b71402
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMFMediaEngineOPMInfo, IMFMediaEngineOPMInfo interface [Media Foundation], IMFMediaEngineOPMInfo interface [Media Foundation],described, mf.imfmediaengineopminfo, mfmediaengine/IMFMediaEngineOPMInfo
ms.topic: interface
f1_keywords: 
 - "mfmediaengine/IMFMediaEngineOPMInfo"
req.header: mfmediaengine.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mfmediaengine.idl
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
 - mfmediaengine.h
api_name:
 - IMFMediaEngineOPMInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFMediaEngineOPMInfo interface


## -description


Provides methods for getting information about the   <a href="https://docs.microsoft.com/windows/desktop/medfound/output-protection-manager">Output Protection Manager</a>  (OPM).


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFMediaEngineOPMInfo</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFMediaEngineOPMInfo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFMediaEngineOPMInfo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineopminfo-getopminfo">GetOPMInfo</a>
</td>
<td align="left" width="63%">
Gets status information about the   <a href="https://docs.microsoft.com/windows/desktop/medfound/output-protection-manager">Output Protection Manager</a>  (OPM).

</td>
</tr>
</table> 


## -remarks



To get a pointer to this interface, call <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q_)">QueryInterface</a> on the Media Engine.

The <b>MF_MEDIA_ENGINE_EVENT_OPMINFO</b> <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent">IMFMediaEvent</a> event is raised when there is a change in the OPM status.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
 

 

