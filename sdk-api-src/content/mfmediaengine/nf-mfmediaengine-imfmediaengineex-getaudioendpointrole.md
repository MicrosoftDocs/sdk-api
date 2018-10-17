---
UID: NF:mfmediaengine.IMFMediaEngineEx.GetAudioEndpointRole
title: IMFMediaEngineEx::GetAudioEndpointRole
author: windows-sdk-content
description: Gets the audio device endpoint role used for the next call to SetSource or Load.
old-location: mf\imfmediaengineex_getaudioendpointrole.htm
tech.root: medfound
ms.assetid: f63fa14e-44e6-41b9-a8c9-4b8eb66e98e0
ms.author: windowssdkdev
ms.date: 10/16/2018
ms.keywords: GetAudioEndpointRole, GetAudioEndpointRole method [Media Foundation], GetAudioEndpointRole method [Media Foundation],IMFMediaEngineEx interface, IMFMediaEngineEx interface [Media Foundation],GetAudioEndpointRole method, IMFMediaEngineEx.GetAudioEndpointRole, IMFMediaEngineEx::GetAudioEndpointRole, mf.imfmediaengineex_getaudioendpointrole, mfmediaengine/IMFMediaEngineEx::GetAudioEndpointRole
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
 - IMFMediaEngineEx.GetAudioEndpointRole
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFMediaEngineEx::GetAudioEndpointRole


## -description


Gets the audio device endpoint role used for the next  call to <a href="https://msdn.microsoft.com/80C41EAB-9B8F-4723-A4A7-A17F56FF5773">SetSource</a> or <a href="https://msdn.microsoft.com/5ACE8143-DC14-495C-A644-A2076FB1980F">Load</a>. 


## -parameters




### -param pRole [out]

Receives the audio endpoint role.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



For information on audio endpoint roles, see <a href="https://msdn.microsoft.com/0d0d3174-8489-4951-858c-024d58477ae0">ERole  enumeration</a>.




## -see-also




<a href="https://msdn.microsoft.com/EE3591FD-4FE8-4F20-A4E2-52C896229571">IMFMediaEngineEx</a>
 

 

