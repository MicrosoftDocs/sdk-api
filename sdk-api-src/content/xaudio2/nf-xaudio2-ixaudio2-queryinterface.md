---
UID: NF:xaudio2.IXAudio2.QueryInterface
title: IXAudio2::QueryInterface (xaudio2.h)
description: Queries for a given COM interface on the XAudio2 object.
helpviewer_keywords: ["IXAudio2 interface [XAudio2 Audio Mixing APIs]","QueryInterface method","IXAudio2.QueryInterface","IXAudio2::QueryInterface","QueryInterface","QueryInterface method [XAudio2 Audio Mixing APIs]","QueryInterface method [XAudio2 Audio Mixing APIs]","IXAudio2 interface","xaudio2.ixaudio2_interface_queryinterface","xaudio2/IXAudio2::QueryInterface"]
old-location: xaudio2\ixaudio2_interface_queryinterface.htm
tech.root: xaudio2
ms.assetid: M:Microsoft.directx_sdk.ixaudio2.IXAudio2.QueryInterface(REFIID,void@)
ms.date: 12/05/2018
ms.keywords: IXAudio2 interface [XAudio2 Audio Mixing APIs],QueryInterface method, IXAudio2.QueryInterface, IXAudio2::QueryInterface, QueryInterface, QueryInterface method [XAudio2 Audio Mixing APIs], QueryInterface method [XAudio2 Audio Mixing APIs],IXAudio2 interface, xaudio2.ixaudio2_interface_queryinterface, xaudio2/IXAudio2::QueryInterface
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
 - IXAudio2::QueryInterface
 - xaudio2/IXAudio2::QueryInterface
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
 - IXAudio2.QueryInterface
---

# IXAudio2::QueryInterface


## -description

Queries for a given COM interface on the XAudio2 object.

## -parameters

### -param riid [in]

The REFIID that identifies the interface to query for.

### -param ppvInterface [out]

Address of a pointer that receives the interface.

## -returns

Returns S_OK if successful, an error code otherwise. See <a href="/windows/desktop/xaudio2/xaudio2-error-codes">XAudio2 Error Codes</a> for descriptions of XAudio2 specific error codes.

## -remarks

Only IID_IUnknown and IID_IXAudio2 are provided by XAudio2.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)

## -see-also

<a href="/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2">IXAudio2</a>