---
UID: NF:xaudio2.IXAudio2SourceVoice.ExitLoop
title: IXAudio2SourceVoice::ExitLoop
author: windows-sdk-content
description: Stops looping the voice when it reaches the end of the current loop region.
old-location: xaudio2\ixaudio2sourcevoice_interface_exitloop.htm
old-project: xaudio2
ms.assetid: M:Microsoft.directx_sdk.ixaudio2sourcevoice.IXAudio2SourceVoice.ExitLoop(UINT32)
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: ExitLoop, ExitLoop method [XAudio2 Audio Mixing APIs], ExitLoop method [XAudio2 Audio Mixing APIs],IXAudio2SourceVoice interface, IXAudio2SourceVoice interface [XAudio2 Audio Mixing APIs],ExitLoop method, IXAudio2SourceVoice.ExitLoop, IXAudio2SourceVoice::ExitLoop, xaudio2.ixaudio2sourcevoice_interface_exitloop, xaudio2/IXAudio2SourceVoice::ExitLoop
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: xaudio2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.typenames: XAUDIO2_FILTER_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - xaudio2.h
api_name:
 - IXAudio2SourceVoice.ExitLoop
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXAudio2SourceVoice::ExitLoop


## -description


Stops looping the voice when it reaches the end of the current loop region. 


## -parameters




### -param X2DEFAULT






#### - OperationSet [in]

Identifies this call as part of a deferred batch. See the <a href="https://msdn.microsoft.com/5bfd747d-af65-f619-e549-be8130748261">XAudio2 Operation Sets</a> overview for more information.


## -returns



Returns S_OK if successful, an error code otherwise. See <a href="https://msdn.microsoft.com/42a1c21c-4b14-114a-d79e-15a61eb2139b">XAudio2 Error Codes</a> for descriptions of XAudio2 specific error codes.




## -remarks



If the cursor for the voice is not in a loop region, <b>ExitLoop</b> does nothing.



<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)




## -see-also




<a href="https://msdn.microsoft.com/library/Ee415914(v=VS.85).aspx">IXAudio2SourceVoice</a>
 

 

