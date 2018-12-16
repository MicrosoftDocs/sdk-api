---
UID: NN:mfmediaengine.IMFMediaEngineOPMInfo
title: IMFMediaEngineOPMInfo
author: windows-sdk-content
description: Provides methods for getting information about the Output Protection Manager (OPM).
old-location: mf\imfmediaengineopminfo.htm
tech.root: medfound
ms.assetid: 399f81ac-38f8-4aaa-8b34-f5fd13b71402
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IMFMediaEngineOPMInfo, IMFMediaEngineOPMInfo interface [Media Foundation], IMFMediaEngineOPMInfo interface [Media Foundation],described, mf.imfmediaengineopminfo, mfmediaengine/IMFMediaEngineOPMInfo
ms.topic: interface
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
---

# IMFMediaEngineOPMInfo interface


## -description


Provides methods for getting information about the   <a href="https://msdn.microsoft.com/daae615b-37c4-4044-91c6-693357e0016a">Output Protection Manager</a>  (OPM).


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFMediaEngineOPMInfo</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFMediaEngineOPMInfo</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/5e4a6e8f-5042-4de1-8cea-64b8e6cc928a">GetOPMInfo</a>
</td>
<td align="left" width="63%">
Gets status information about the   <a href="https://msdn.microsoft.com/daae615b-37c4-4044-91c6-693357e0016a">Output Protection Manager</a>  (OPM).

</td>
</tr>
</table> 


## -remarks



To get a pointer to this interface, call <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> on the Media Engine.

The <b>MF_MEDIA_ENGINE_EVENT_OPMINFO</b> <a href="https://msdn.microsoft.com/b4f686be-9472-433c-b983-6c48dfd3ac76">IMFMediaEvent</a> event is raised when there is a change in the OPM status.




## -see-also




<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>
 

 

