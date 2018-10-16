---
UID: NF:mfmediaengine.IMFMediaEngine.Load
title: IMFMediaEngine::Load
author: windows-sdk-content
description: Loads the current media source.
old-location: mf\imfmediaengine_load.htm
tech.root: medfound
ms.assetid: 5ACE8143-DC14-495C-A644-A2076FB1980F
ms.author: windowssdkdev
ms.date: 10/15/2018
ms.keywords: IMFMediaEngine interface [Media Foundation],Load method, IMFMediaEngine.Load, IMFMediaEngine::Load, Load, Load method [Media Foundation], Load method [Media Foundation],IMFMediaEngine interface, mf.imfmediaengine_load, mfmediaengine/IMFMediaEngine::Load
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfmediaengine.h
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
 - mfmediaengine.h
api_name:
 - IMFMediaEngine.Load
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFMediaEngine::Load


## -description


Loads the current media source.


## -parameters






## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The main purpose of this method is to reload a list of source elements after updating the list. For more information, see <a href="https://msdn.microsoft.com/7B1A1C43-A9BD-4DBF-B6A7-53BF9295CDAC">SetSourceElements</a>. Otherwise, calling this method is generally not required. To load a new media source, call <a href="https://msdn.microsoft.com/80C41EAB-9B8F-4723-A4A7-A17F56FF5773">IMFMediaEngine::SetSource</a> or <b>IMFMediaEngine::SetSourceElements</b>.

The <b>Load</b>  method explictly invokes the Media Engine's media resource loading algorithm. Before calling this method, you must set the media resource by calling <a href="https://msdn.microsoft.com/80C41EAB-9B8F-4723-A4A7-A17F56FF5773">IMFMediaEngine::SetSource</a> or <a href="https://msdn.microsoft.com/7B1A1C43-A9BD-4DBF-B6A7-53BF9295CDAC">IMFMediaEngine::SetSourceElements</a>. 

This method completes asynchronously. When the <b>Load</b> operation starts, the Media Engine sends an <b>MF_MEDIA_ENGINE_EVENT_LOADSTART</b> event. If no errors occur during the <b>Load</b> operation, several other events are generated, including the following.

<ul>
<li><b>MF_MEDIA_ENGINE_EVENT_LOADEDMETADATA</b></li>
<li><b>MF_MEDIA_ENGINE_EVENT_LOADEDDATA</b></li>
<li><b>MF_MEDIA_ENGINE_EVENT_CANPLAY</b></li>
<li><b>MF_MEDIA_ENGINE_EVENT_CANPLAYTHROUGH</b></li>
</ul>
If the Media Engine is unable to load the file, the Media Engine sends an <b>MF_MEDIA_ENGINE_EVENT_ERROR</b> event. 

For more information about event handling in the Media Engine, see <a href="https://msdn.microsoft.com/85D702D4-3C9B-4848-81F2-3634C2B6AE1A">IMFMediaEngineNotify</a>.

This method corresponds to the <b>load</b> method of the <b>HTMLMediaElement</b> interface in HTML5. 




## -see-also




<a href="https://msdn.microsoft.com/A0023F18-2D28-4F0D-9B00-B8FB11567034">IMFMediaEngine</a>
 

 

