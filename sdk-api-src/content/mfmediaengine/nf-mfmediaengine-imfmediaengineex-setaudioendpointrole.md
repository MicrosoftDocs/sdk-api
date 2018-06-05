---
UID: NF:mfmediaengine.IMFMediaEngineEx.SetAudioEndpointRole
title: IMFMediaEngineEx::SetAudioEndpointRole
author: windows-sdk-content
description: Sets the audio device endpoint used for the next call to SetSource or Load.
old-location: mf\imfmediaengineex_setaudioendpointrole.htm
old-project: medfound
ms.assetid: 00fd78ce-e046-40a0-8bad-f4a1e1f517bb
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: IMFMediaEngineEx interface [Media Foundation],SetAudioEndpointRole method, IMFMediaEngineEx.SetAudioEndpointRole, IMFMediaEngineEx::SetAudioEndpointRole, SetAudioEndpointRole, SetAudioEndpointRole method [Media Foundation], SetAudioEndpointRole method [Media Foundation],IMFMediaEngineEx interface, mf.imfmediaengineex_setaudioendpointrole, mfmediaengine/IMFMediaEngineEx::SetAudioEndpointRole
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
tech.root: 
req.typenames: MF_TIMED_TEXT_WRITING_MODE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfmediaengine.h
api_name:
-	IMFMediaEngineEx.SetAudioEndpointRole
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFMediaEngineEx::SetAudioEndpointRole


## -description


Sets the audio device endpoint used for the next call to <a href="https://msdn.microsoft.com/80C41EAB-9B8F-4723-A4A7-A17F56FF5773">SetSource</a> or <a href="https://msdn.microsoft.com/5ACE8143-DC14-495C-A644-A2076FB1980F">Load</a>. 


## -parameters




### -param role [in]

Specifies the audio end point role.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



For information on audio endpoint roles, see <a href="https://msdn.microsoft.com/0d0d3174-8489-4951-858c-024d58477ae0">ERole  enumeration</a>.




## -see-also




<a href="https://msdn.microsoft.com/EE3591FD-4FE8-4F20-A4E2-52C896229571">IMFMediaEngineEx</a>
 

 

