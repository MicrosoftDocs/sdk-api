---
UID: NF:d3d11.ID3D11VideoContext.StartSessionKeyRefresh
title: ID3D11VideoContext::StartSessionKeyRefresh (d3d11.h)
description: Gets a random number that can be used to refresh the session key. (ID3D11VideoContext.StartSessionKeyRefresh)
helpviewer_keywords: ["ID3D11VideoContext interface [Media Foundation]","StartSessionKeyRefresh method","ID3D11VideoContext.StartSessionKeyRefresh","ID3D11VideoContext::StartSessionKeyRefresh","StartSessionKeyRefresh","StartSessionKeyRefresh method [Media Foundation]","StartSessionKeyRefresh method [Media Foundation]","ID3D11VideoContext interface","d3d11/ID3D11VideoContext::StartSessionKeyRefresh","mf.id3d11videocontext_startsessionkeyrefresh"]
old-location: mf\id3d11videocontext_startsessionkeyrefresh.htm
tech.root: mf
ms.assetid: 63376BFE-BA84-4268-8AA8-128BEB83AE78
ms.date: 12/05/2018
ms.keywords: ID3D11VideoContext interface [Media Foundation],StartSessionKeyRefresh method, ID3D11VideoContext.StartSessionKeyRefresh, ID3D11VideoContext::StartSessionKeyRefresh, StartSessionKeyRefresh, StartSessionKeyRefresh method [Media Foundation], StartSessionKeyRefresh method [Media Foundation],ID3D11VideoContext interface, d3d11/ID3D11VideoContext::StartSessionKeyRefresh, mf.id3d11videocontext_startsessionkeyrefresh
req.header: d3d11.h
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D11VideoContext::StartSessionKeyRefresh
 - d3d11/ID3D11VideoContext::StartSessionKeyRefresh
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d11.h
api_name:
 - ID3D11VideoContext.StartSessionKeyRefresh
---

# ID3D11VideoContext::StartSessionKeyRefresh


## -description

Gets a random number that can be used to refresh the session key.

## -parameters

### -param pCryptoSession [in]

A pointer to the <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11cryptosession">ID3D11CryptoSession</a> interface.

### -param RandomNumberSize [in]

The size of the <i>pRandomNumber</i> array, in bytes. The size should match the size of the session key.

### -param pRandomNumber [out]

A pointer to a byte array that receives a random number.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

To generate a new session key, perform a bitwise <b>XOR</b> between the previous session key and the random number. The new session key does not take affect until the application calls <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-finishsessionkeyrefresh">ID3D11VideoContext::FinishSessionKeyRefresh</a>.

To query whether the driver supports this method, call <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-getcontentprotectioncaps">ID3D11VideoDevice::GetContentProtectionCaps</a> and check for the <b>D3D11_CONTENT_PROTECTION_CAPS_FRESHEN_SESSION_KEY</b> capabilities flag.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11videocontext">ID3D11VideoContext</a>
