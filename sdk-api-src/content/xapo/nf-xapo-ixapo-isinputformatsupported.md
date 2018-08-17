---
UID: NF:xapo.IXAPO.IsInputFormatSupported
title: IXAPO::IsInputFormatSupported
author: windows-sdk-content
description: Queries if a specific input format is supported for a given output format.
old-location: xaudio2\ixapo_interface_isinputformatsupported.htm
old-project: xaudio2
ms.assetid: M:Microsoft.directx_sdk.ixapo.IXAPO.IsInputFormatSupported(const WAVEFORMATEX,const WAVEFORMATEX,WAVEFORMATEX)
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IXAPO interface [XAudio2 Audio Mixing APIs],IsInputFormatSupported method, IXAPO.IsInputFormatSupported, IXAPO::IsInputFormatSupported, IsInputFormatSupported, IsInputFormatSupported method [XAudio2 Audio Mixing APIs], IsInputFormatSupported method [XAudio2 Audio Mixing APIs],IXAPO interface, xapo/IXAPO::IsInputFormatSupported, xaudio2.ixapo_interface_isinputformatsupported
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: xapo.h
req.include-header: 
req.redist: 
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
req.typenames: XAPO_BUFFER_FLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - XAPO.h
api_name:
 - IXAPO.IsInputFormatSupported
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXAPO::IsInputFormatSupported


## -description


Queries if a specific input format is supported for a given output format.


## -parameters




### -param pOutputFormat

Output format.



### -param pRequestedInputFormat

Input format to check for being supported.


### -param ppSupportedInputFormat

If not NULL, and the input format is not supported for the given output format, <i>ppSupportedInputFormat</i> returns a pointer to the closest input format that is supported. Use <a href="https://msdn.microsoft.com/7E24273A-483B-42E5-8428-A9ED7DD04561">XAPOFree</a> to free the returned structure. 


## -returns



Returns S_OK if the format pair is supported. Returns XAPO_E_FORMAT_UNSUPPORTED if the format pair is not supported.




## -remarks



The <a href="https://msdn.microsoft.com/5921C1C2-91DF-4E1F-A179-786CEB997BAF">IXAPO::IsOutputFormatSupported</a> and <b>IsInputFormatSupported</b> methods allow an XAPO to indicate which audio formats it is capable of processing. If a requested format is not supported, the XAPO should return the closest format that it does support. The closest format should be determined based on frame rate, bit depth, and channel count, in that order of importance. The behavior of <b>IsInputFormatSupported</b> is allowed to change, based on the internal state of the XAPO, but its behavior should remain constant between calls to the <a href="https://msdn.microsoft.com/2143A204-342F-4A78-A6D7-D319360A3948">IXAPO::LockForProcess</a> and <a href="https://msdn.microsoft.com/1D70B361-6EB6-4591-9AD2-2E802F6EE341">IXAPO::UnlockForProcess</a> methods.



<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)




## -see-also




<a href="https://msdn.microsoft.com/21DA61D2-8EDE-496B-8513-D67121697FBA">IXAPO</a>
 

 

