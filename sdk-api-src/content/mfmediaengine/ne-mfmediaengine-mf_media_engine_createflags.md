---
UID: NE:mfmediaengine.MF_MEDIA_ENGINE_CREATEFLAGS
title: MF_MEDIA_ENGINE_CREATEFLAGS
author: windows-sdk-content
description: Contains flags for the IMFMediaEngineClassFactory::CreateInstance method.
old-location: mf\mf_media_engine_createflags.htm
old-project: medfound
ms.assetid: 1709B08C-D4DC-4A33-9B92-1C4961208684
ms.author: windowssdkdev
ms.date: 06/05/2018
ms.keywords: MF_MEDIA_ENGINE_AUDIOONLY, MF_MEDIA_ENGINE_CREATEFLAGS, MF_MEDIA_ENGINE_CREATEFLAGS enumeration [Media Foundation], MF_MEDIA_ENGINE_CREATEFLAGS_MASK, MF_MEDIA_ENGINE_DISABLE_LOCAL_PLUGINS, MF_MEDIA_ENGINE_FORCEMUTE, MF_MEDIA_ENGINE_REAL_TIME_MODE, MF_MEDIA_ENGINE_WAITFORSTABLE_STATE, mf.mf_media_engine_createflags, mfmediaengine/MF_MEDIA_ENGINE_AUDIOONLY, mfmediaengine/MF_MEDIA_ENGINE_CREATEFLAGS, mfmediaengine/MF_MEDIA_ENGINE_CREATEFLAGS_MASK, mfmediaengine/MF_MEDIA_ENGINE_DISABLE_LOCAL_PLUGINS, mfmediaengine/MF_MEDIA_ENGINE_FORCEMUTE, mfmediaengine/MF_MEDIA_ENGINE_REAL_TIME_MODE, mfmediaengine/MF_MEDIA_ENGINE_WAITFORSTABLE_STATE
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
tech.root: 
req.typenames: MF_MEDIA_ENGINE_CREATEFLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mfmediaengine.h
api_name:
 - MF_MEDIA_ENGINE_CREATEFLAGS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# MF_MEDIA_ENGINE_CREATEFLAGS enumeration


## -description


Contains flags for the <a href="https://msdn.microsoft.com/EDEAD2C4-5695-4E63-9E9E-B09D75B60B7F">IMFMediaEngineClassFactory::CreateInstance</a>  method.


## -enum-fields




### -field MF_MEDIA_ENGINE_AUDIOONLY

The Media Engine will play audio only. It will not play video.


### -field MF_MEDIA_ENGINE_WAITFORSTABLE_STATE

The Media Engine's resource loading algorithm waits for the application to signal the thread that loads the resource. For more information, see the remarks for <b>MF_MEDIA_ENGINE_EVENT_NOTIFYSTABLESTATE</b> in the <a href="https://msdn.microsoft.com/05790FF8-0720-474B-AFF1-362E7A1B7C34">MF_MEDIA_ENGINE_EVENT</a> enumeration.


### -field MF_MEDIA_ENGINE_FORCEMUTE

Always mute the audio.


### -field MF_MEDIA_ENGINE_REAL_TIME_MODE

Enable low-latency mode in the rendering pipeline. This can be changed at a later time by calling <a href="https://msdn.microsoft.com/31534f69-33ec-41d3-93aa-f4c457649e48">IMFMediaEngineEx::SetRealTimeMode</a>.


### -field MF_MEDIA_ENGINE_DISABLE_LOCAL_PLUGINS

Disable locally registered media plugins. If this flag is set, the Media Engine will not load decoders or other media plugins that the application registered for the local process.


### -field MF_MEDIA_ENGINE_CREATEFLAGS_MASK

Reserved.


## -see-also




<a href="https://msdn.microsoft.com/f26a730f-18c4-4247-acaf-af1dfad19086">Media Foundation Enumerations</a>
 

 

