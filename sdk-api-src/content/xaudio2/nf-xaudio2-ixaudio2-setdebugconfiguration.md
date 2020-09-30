---
UID: NF:xaudio2.IXAudio2.SetDebugConfiguration
title: IXAudio2::SetDebugConfiguration (xaudio2.h)
description: Changes global debug logging options for XAudio2.
helpviewer_keywords: ["IXAudio2 interface [XAudio2 Audio Mixing APIs]","SetDebugConfiguration method","IXAudio2.SetDebugConfiguration","IXAudio2::SetDebugConfiguration","SetDebugConfiguration","SetDebugConfiguration method [XAudio2 Audio Mixing APIs]","SetDebugConfiguration method [XAudio2 Audio Mixing APIs]","IXAudio2 interface","xaudio2.ixaudio2_interface_setdebugconfiguration","xaudio2/IXAudio2::SetDebugConfiguration"]
old-location: xaudio2\ixaudio2_interface_setdebugconfiguration.htm
tech.root: xaudio2
ms.assetid: M:Microsoft.directx_sdk.ixaudio2.IXAudio2.SetDebugConfiguration(XAUDIO2_DEBUG_CONFIGURATION)
ms.date: 12/05/2018
ms.keywords: IXAudio2 interface [XAudio2 Audio Mixing APIs],SetDebugConfiguration method, IXAudio2.SetDebugConfiguration, IXAudio2::SetDebugConfiguration, SetDebugConfiguration, SetDebugConfiguration method [XAudio2 Audio Mixing APIs], SetDebugConfiguration method [XAudio2 Audio Mixing APIs],IXAudio2 interface, xaudio2.ixaudio2_interface_setdebugconfiguration, xaudio2/IXAudio2::SetDebugConfiguration
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IXAudio2::SetDebugConfiguration
 - xaudio2/IXAudio2::SetDebugConfiguration
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - xaudio2.h
api_name:
 - IXAudio2.SetDebugConfiguration
---

# IXAudio2::SetDebugConfiguration


## -description

Changes global debug logging options for XAudio2.

## -parameters

### -param pDebugConfiguration

Pointer to a <a href="/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_debug_configuration">XAUDIO2_DEBUG_CONFIGURATION</a> structure that contains the new debug configuration.

### -param X2DEFAULT

This parameter is reserved and must be NULL.

## -remarks

SetDebugConfiguration sets the debug configuration for the given instance of XAudio2 engine. See <a href="/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_debug_configuration">XAUDIO2_DEBUG_CONFIGURATION</a> Structure for supported debug options. By default, XAudio2 does not log debug output or break on errors. 

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)

## -see-also

<a href="/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2">IXAudio2</a>



<a href="/windows/desktop/xaudio2/functions">XAudio2 Functions</a>