---
UID: NF:xapo.IXAPO.IsOutputFormatSupported
title: IXAPO::IsOutputFormatSupported
author: windows-sdk-content
description: Queries if a specific output format is supported for a given input format.
old-location: xaudio2\ixapo_interface_isoutputformatsupported.htm
old-project: xaudio2
ms.assetid: M:Microsoft.directx_sdk.ixapo.IXAPO.IsOutputFormatSupported(const WAVEFORMATEX,const WAVEFORMATEX,WAVEFORMATEX@)
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IXAPO interface [XAudio2 Audio Mixing APIs],IsOutputFormatSupported method, IXAPO.IsOutputFormatSupported, IXAPO::IsOutputFormatSupported, IsOutputFormatSupported, IsOutputFormatSupported method [XAudio2 Audio Mixing APIs], IsOutputFormatSupported method [XAudio2 Audio Mixing APIs],IXAPO interface, xapo/IXAPO::IsOutputFormatSupported, xaudio2.ixapo_interface_isoutputformatsupported
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
 - IXAPO.IsOutputFormatSupported
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXAPO::IsOutputFormatSupported


## -description


Queries if a specific output format is supported for a given input format.


## -parameters




### -param pInputFormat [in]

Input format. 


### -param pRequestedOutputFormat [in]

Output format to check for being supported.


### -param ppSupportedOutputFormat [out]

If not NULL and the output format is not supported for the given input format, <i>ppSupportedOutputFormat</i> returns a pointer to the closest output format that is supported. Use <a href="https://msdn.microsoft.com/en-us/library/Ee419206(v=VS.85).aspx">XAPOFree</a> to free the returned structure. 


## -returns



Returns S_OK if the format pair is supported. Returns XAPO_E_FORMAT_UNSUPPORTED if the format pair is not supported.




## -remarks



The <a href="https://msdn.microsoft.com/en-us/library/Ee418453(v=VS.85).aspx">IXAPO::IsInputFormatSupported</a> and <b>IsOutputFormatSupported</b> methods allow an XAPO to indicate which audio formats it is capable of processing. If a requested format is not supported, the XAPO should return the closest format that it does support. The closest format should be determined based on frame rate, bit depth, and channel count, in that order of importance. The behavior of <b>IsOutputFormatSupported</b> is allowed to change, based on the internal state of the XAPO, but its behavior should remain constant between calls to the <a href="https://msdn.microsoft.com/en-us/library/Ee418455(v=VS.85).aspx">IXAPO::LockForProcess</a> and <a href="https://msdn.microsoft.com/en-us/library/Ee418460(v=VS.85).aspx">IXAPO::UnlockForProcess</a> methods.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Ee415893(v=VS.85).aspx">IXAPO</a>
 

 

