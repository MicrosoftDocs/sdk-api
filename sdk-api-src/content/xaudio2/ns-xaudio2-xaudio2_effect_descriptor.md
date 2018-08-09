---
UID: NS:xaudio2.XAUDIO2_EFFECT_DESCRIPTOR
title: XAUDIO2_EFFECT_DESCRIPTOR
author: windows-sdk-content
description: Contains information about an XAPO for use in an effect chain.
old-location: xaudio2\xaudio2_effect_descriptor.htm
old-project: xaudio2
ms.assetid: T:Microsoft.directx_sdk.xaudio2.XAUDIO2_EFFECT_DESCRIPTOR
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: XAUDIO2_EFFECT_DESCRIPTOR, XAUDIO2_EFFECT_DESCRIPTOR structure [XAudio2 Audio Mixing APIs], xaudio2.xaudio2_effect_descriptor, xaudio2/XAUDIO2_EFFECT_DESCRIPTOR
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
req.typenames: XAUDIO2_EFFECT_DESCRIPTOR
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - xaudio2.h
api_name:
 - XAUDIO2_EFFECT_DESCRIPTOR
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# XAUDIO2_EFFECT_DESCRIPTOR structure


## -description


Contains information about an <a href="https://msdn.microsoft.com/4fe88a0f-0234-462f-b575-e592f2c8401e">XAPO</a> for use in an effect chain.


## -struct-fields




### -field pEffect

Pointer to the <b>IUnknown</b> interface of the <a href="https://msdn.microsoft.com/4fe88a0f-0234-462f-b575-e592f2c8401e">XAPO</a> object.


### -field InitialState

TRUE if the effect should begin in the enabled state. Otherwise, FALSE.


### -field OutputChannels

Number of output channels the effect should produce.


## -remarks



XAPO instances are passed to XAudio2 as <b>IUnknown</b> interfaces and XAudio2 uses <a href="https://msdn.microsoft.com/730A07AF-FCD9-4BF3-BFD1-28DA8D91876F">IXAPO::QueryInterface</a> to acquire an <a href="https://msdn.microsoft.com/en-us/library/Ee415893(v=VS.85).aspx">IXAPO</a> interface and to detect whether the XAPO implements the <a href="https://msdn.microsoft.com/en-us/library/Ee415896(v=VS.85).aspx">IXAPOParameters</a> interface.



For additional information on using XAPOs with XAudio2 see <a href="https://msdn.microsoft.com/4c33bd83-2654-cd6f-ea6c-bbc0d5872638">How to: Create an Effect Chain</a> and <a href="https://msdn.microsoft.com/d4d24177-25eb-13ca-0e38-0c876a273e0d">How to: Use an XAPO in XAudio2</a>.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)




## -see-also




<a href="https://msdn.microsoft.com/4fe88a0f-0234-462f-b575-e592f2c8401e">XAPO Overview</a>



<a href="https://msdn.microsoft.com/3656aaf9-7a3a-2a5b-50f5-d279ce8a9e6c">XAudio2 Structures</a>



<a href="https://msdn.microsoft.com/en-us/library/Ee419235(v=VS.85).aspx">XAudio2_Effect_Chain</a>
 

 

