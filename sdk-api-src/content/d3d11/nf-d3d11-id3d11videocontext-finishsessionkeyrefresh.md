---
UID: NF:d3d11.ID3D11VideoContext.FinishSessionKeyRefresh
title: ID3D11VideoContext::FinishSessionKeyRefresh (d3d11.h)
description: Switches to a new session key. (ID3D11VideoContext.FinishSessionKeyRefresh)
helpviewer_keywords: ["FinishSessionKeyRefresh","FinishSessionKeyRefresh method [Media Foundation]","FinishSessionKeyRefresh method [Media Foundation]","ID3D11VideoContext interface","ID3D11VideoContext interface [Media Foundation]","FinishSessionKeyRefresh method","ID3D11VideoContext.FinishSessionKeyRefresh","ID3D11VideoContext::FinishSessionKeyRefresh","d3d11/ID3D11VideoContext::FinishSessionKeyRefresh","mf.id3d11videocontext_finishsessionkeyrefresh"]
old-location: mf\id3d11videocontext_finishsessionkeyrefresh.htm
tech.root: mf
ms.assetid: 2F602A5E-B5D1-4749-8696-9F0594770B4F
ms.date: 12/05/2018
ms.keywords: FinishSessionKeyRefresh, FinishSessionKeyRefresh method [Media Foundation], FinishSessionKeyRefresh method [Media Foundation],ID3D11VideoContext interface, ID3D11VideoContext interface [Media Foundation],FinishSessionKeyRefresh method, ID3D11VideoContext.FinishSessionKeyRefresh, ID3D11VideoContext::FinishSessionKeyRefresh, d3d11/ID3D11VideoContext::FinishSessionKeyRefresh, mf.id3d11videocontext_finishsessionkeyrefresh
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
 - ID3D11VideoContext::FinishSessionKeyRefresh
 - d3d11/ID3D11VideoContext::FinishSessionKeyRefresh
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
 - ID3D11VideoContext.FinishSessionKeyRefresh
---

# ID3D11VideoContext::FinishSessionKeyRefresh


## -description

Switches to a new session key.

## -parameters

### -param pCryptoSession [in]

A pointer to the <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11cryptosession">ID3D11CryptoSession</a> interface.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This function can only be called when the <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_content_protection_caps">D3D11_CONTENT_PROTECTION_CAPS_FRESHEN_SESSION_KEY</a> cap is reported.

Before calling this method, call <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-startsessionkeyrefresh">ID3D11VideoContext::StartSessionKeyRefresh</a>. The <b>StartSessionKeyRefresh</b> method gets a random number from the driver, which is used to create a new session key. The new session key does not become active until the application calls <b>FinishSessionKeyRefresh</b>. After the application calls <b>FinishSessionKeyRefresh</b>, all protected surfaces are encrypted using the new session key.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11videocontext">ID3D11VideoContext</a>
