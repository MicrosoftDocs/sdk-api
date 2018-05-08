---
UID: NF:xaudio2.IXAudio2.SetDebugConfiguration
title: IXAudio2::SetDebugConfiguration
author: windows-driver-content
description: Changes global debug logging options for XAudio2.
old-location: xaudio2\ixaudio2_interface_setdebugconfiguration.htm
old-project: xaudio2
ms.assetid: M:Microsoft.directx_sdk.ixaudio2.IXAudio2.SetDebugConfiguration(XAUDIO2_DEBUG_CONFIGURATION)
ms.author: windowsdriverdev
ms.date: 4/20/2018
ms.keywords: IXAudio2 interface [XAudio2 Audio Mixing APIs],SetDebugConfiguration method, IXAudio2.SetDebugConfiguration, IXAudio2::SetDebugConfiguration, SetDebugConfiguration, SetDebugConfiguration method [XAudio2 Audio Mixing APIs], SetDebugConfiguration method [XAudio2 Audio Mixing APIs],IXAudio2 interface, xaudio2.ixaudio2_interface_setdebugconfiguration, xaudio2/IXAudio2::SetDebugConfiguration
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: XAUDIO2_FILTER_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	xaudio2.h
api_name:
-	IXAudio2.SetDebugConfiguration
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXAudio2::SetDebugConfiguration


## -description


Changes global debug logging options for XAudio2.


## -parameters




### -param pDebugConfiguration

Pointer to a <a href="https://msdn.microsoft.com/92c98bc5-26d3-4815-9234-c3ba7b6eb3c2">XAUDIO2_DEBUG_CONFIGURATION</a> structure that contains the new debug configuration.


### -param X2DEFAULT






#### - pReserved

This parameter is reserved and must be NULL.


## -returns



This method does not return a value.




## -remarks



SetDebugConfiguration sets the debug configuration for the given instance of XAudio2 engine. See <a href="https://msdn.microsoft.com/92c98bc5-26d3-4815-9234-c3ba7b6eb3c2">XAUDIO2_DEBUG_CONFIGURATION</a> Structure for supported debug options. By default, XAudio2 does not log debug output or break on errors. 

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)




## -see-also




<a href="https://msdn.microsoft.com/A49469C6-2C29-407C-8C57-65E3FC9463F1">IXAudio2</a>



<a href="https://msdn.microsoft.com/870a0425-3226-7848-bcc0-0ba7145135cb">XAudio2 Functions</a>
 

 

