---
UID: NF:mfmediaengine.IMFMediaEngine.SetSource
title: IMFMediaEngine::SetSource
author: windows-sdk-content
description: Sets the URL of a media resource.
old-location: mf\imfmediaengine_setsource.htm
old-project: medfound
ms.assetid: 80C41EAB-9B8F-4723-A4A7-A17F56FF5773
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: IMFMediaEngine interface [Media Foundation],SetSource method, IMFMediaEngine.SetSource, IMFMediaEngine::SetSource, SetSource, SetSource method [Media Foundation], SetSource method [Media Foundation],IMFMediaEngine interface, mf.imfmediaengine_setsource, mfmediaengine/IMFMediaEngine::SetSource
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mfmediaengine.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: MF_MEDIA_ENGINE_KEYERR
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfmediaengine.h
api_name:
 - IMFMediaEngine.SetSource
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFMediaEngine::SetSource


## -description


Sets the URL of a media resource.


## -parameters




### -param pUrl [in]

The URL of the media resource.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method corresponds to setting the <b>src</b> attribute of the <b>HTMLMediaElement</b> interface in HTML5.

The URL specified by this method takes precedence over media resources specified in the <a href="https://msdn.microsoft.com/7B1A1C43-A9BD-4DBF-B6A7-53BF9295CDAC">IMFMediaEngine::SetSourceElements</a> method. To load the URL, call <a href="https://msdn.microsoft.com/5ACE8143-DC14-495C-A644-A2076FB1980F">IMFMediaEngine::Load</a>.

This method asynchronously loads the URL. When the operation starts, the Media Engine sends an <b>MF_MEDIA_ENGINE_EVENT_LOADSTART</b> event. If no errors occur during the <a href="https://msdn.microsoft.com/5ACE8143-DC14-495C-A644-A2076FB1980F">Load</a> operation, several other events are generated, including the following.

<ul>
<li><b>MF_MEDIA_ENGINE_EVENT_LOADEDMETADATA</b></li>
<li><b>MF_MEDIA_ENGINE_EVENT_LOADEDDATA</b></li>
<li><b>MF_MEDIA_ENGINE_EVENT_CANPLAY</b></li>
<li><b>MF_MEDIA_ENGINE_EVENT_CANPLAYTHROUGH</b></li>
</ul>
If the Media Engine is unable to load the URL, the Media Engine sends an <b>MF_MEDIA_ENGINE_EVENT_ERROR</b> event. 

For more information about event handling in the Media Engine, see <a href="https://msdn.microsoft.com/85D702D4-3C9B-4848-81F2-3634C2B6AE1A">IMFMediaEngineNotify</a>.




## -see-also




<a href="https://msdn.microsoft.com/A0023F18-2D28-4F0D-9B00-B8FB11567034">IMFMediaEngine</a>
 

 

