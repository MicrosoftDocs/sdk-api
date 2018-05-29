---
UID: NF:mfmediaengine.IMFMediaEngine.SetSourceElements
title: IMFMediaEngine::SetSourceElements
author: windows-sdk-content
description: Sets a list of media sources.
old-location: mf\imfmediaengine_setsourceelements.htm
old-project: medfound
ms.assetid: 7B1A1C43-A9BD-4DBF-B6A7-53BF9295CDAC
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: IMFMediaEngine interface [Media Foundation],SetSourceElements method, IMFMediaEngine.SetSourceElements, IMFMediaEngine::SetSourceElements, SetSourceElements, SetSourceElements method [Media Foundation], SetSourceElements method [Media Foundation],IMFMediaEngine interface, mf.imfmediaengine_setsourceelements, mfmediaengine/IMFMediaEngine::SetSourceElements
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mfmediaengine.h
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
req.typenames: MF_TIMED_TEXT_WRITING_MODE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfmediaengine.h
api_name:
-	IMFMediaEngine.SetSourceElements
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFMediaEngine::SetSourceElements


## -description


Sets a list of media sources.


## -parameters




### -param pSrcElements [in]

A pointer to the <a href="https://msdn.microsoft.com/37A3EAC0-639C-47F3-AAB9-588EBEC8E1E3">IMFMediaEngineSrcElements</a> interface. The caller must implement this interface. 


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method corresponds to adding a list of <b>source</b> elements to a media element in HTML5. 

The Media Engine tries to load each item in the <i>pSrcElements</i> list, until it finds one that loads successfully. After this method is called, the application can use the <a href="https://msdn.microsoft.com/37A3EAC0-639C-47F3-AAB9-588EBEC8E1E3">IMFMediaEngineSrcElements</a> interface to update the list at any time. To reload the list, call <a href="https://msdn.microsoft.com/5ACE8143-DC14-495C-A644-A2076FB1980F">IMFMediaEngine::Load</a>.

This method completes asynchronously. When the operation starts, the Media Engine sends an <b>MF_MEDIA_ENGINE_EVENT_LOADSTART</b> event. If no errors occur during the <a href="https://msdn.microsoft.com/5ACE8143-DC14-495C-A644-A2076FB1980F">Load</a> operation, several other events are generated, including the following.

<ul>
<li><b>MF_MEDIA_ENGINE_EVENT_LOADEDMETADATA</b></li>
<li><b>MF_MEDIA_ENGINE_EVENT_LOADEDDATA</b></li>
<li><b>MF_MEDIA_ENGINE_EVENT_CANPLAY</b></li>
<li><b>MF_MEDIA_ENGINE_EVENT_CANPLAYTHROUGH</b></li>
</ul>
If the Media Engine is unable to load a URL, it sends an <b>MF_MEDIA_ENGINE_EVENT_ERROR</b> event. 

For more information about event handling in the Media Engine, see <a href="https://msdn.microsoft.com/85D702D4-3C9B-4848-81F2-3634C2B6AE1A">IMFMediaEngineNotify</a>.

If the application also calls <a href="https://msdn.microsoft.com/80C41EAB-9B8F-4723-A4A7-A17F56FF5773">IMFMediaEngine::SetSource</a>, the URL passed to <b>SetSource</b> takes precedence over the list given to <b>SetSourceElements</b>.




## -see-also




<a href="https://msdn.microsoft.com/A0023F18-2D28-4F0D-9B00-B8FB11567034">IMFMediaEngine</a>
 

 

