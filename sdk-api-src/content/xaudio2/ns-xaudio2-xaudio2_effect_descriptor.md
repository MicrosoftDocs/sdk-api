---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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



XAPO instances are passed to XAudio2 as <b>IUnknown</b> interfaces and XAudio2 uses <a href="https://msdn.microsoft.com/730A07AF-FCD9-4BF3-BFD1-28DA8D91876F">IXAPO::QueryInterface</a> to acquire an <a href="https://msdn.microsoft.com/21DA61D2-8EDE-496B-8513-D67121697FBA">IXAPO</a> interface and to detect whether the XAPO implements the <a href="https://msdn.microsoft.com/0CB2BA7E-5115-449C-A538-44EDCAFFE96F">IXAPOParameters</a> interface.



For additional information on using XAPOs with XAudio2 see <a href="https://msdn.microsoft.com/4c33bd83-2654-cd6f-ea6c-bbc0d5872638">How to: Create an Effect Chain</a> and <a href="https://msdn.microsoft.com/d4d24177-25eb-13ca-0e38-0c876a273e0d">How to: Use an XAPO in XAudio2</a>.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)




## -see-also




<a href="https://msdn.microsoft.com/4fe88a0f-0234-462f-b575-e592f2c8401e">XAPO Overview</a>



<a href="https://msdn.microsoft.com/3656aaf9-7a3a-2a5b-50f5-d279ce8a9e6c">XAudio2 Structures</a>



<a href="https://msdn.microsoft.com/7519f0e0-e063-4849-ba58-675f42e91241">XAudio2_Effect_Chain</a>
 

 

