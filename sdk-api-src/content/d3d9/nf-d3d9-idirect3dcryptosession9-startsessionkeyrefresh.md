---
UID: NF:d3d9.IDirect3DCryptoSession9.StartSessionKeyRefresh
title: IDirect3DCryptoSession9::StartSessionKeyRefresh (d3d9.h)
description: Gets a random number that can be used to refresh the session key. (IDirect3DCryptoSession9.StartSessionKeyRefresh)
helpviewer_keywords: ["IDirect3DCryptoSession9 interface [Media Foundation]","StartSessionKeyRefresh method","IDirect3DCryptoSession9.StartSessionKeyRefresh","IDirect3DCryptoSession9::StartSessionKeyRefresh","StartSessionKeyRefresh","StartSessionKeyRefresh method [Media Foundation]","StartSessionKeyRefresh method [Media Foundation]","IDirect3DCryptoSession9 interface","d3d9/IDirect3DCryptoSession9::StartSessionKeyRefresh","mf.idirect3dcryptosession9_startsessionkeyrefresh"]
old-location: mf\idirect3dcryptosession9_startsessionkeyrefresh.htm
tech.root: mf
ms.assetid: f25ad491-9ffb-40d1-94c3-af0cbae553bf
ms.date: 12/05/2018
ms.keywords: IDirect3DCryptoSession9 interface [Media Foundation],StartSessionKeyRefresh method, IDirect3DCryptoSession9.StartSessionKeyRefresh, IDirect3DCryptoSession9::StartSessionKeyRefresh, StartSessionKeyRefresh, StartSessionKeyRefresh method [Media Foundation], StartSessionKeyRefresh method [Media Foundation],IDirect3DCryptoSession9 interface, d3d9/IDirect3DCryptoSession9::StartSessionKeyRefresh, mf.idirect3dcryptosession9_startsessionkeyrefresh
req.header: d3d9.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - IDirect3DCryptoSession9::StartSessionKeyRefresh
 - d3d9/IDirect3DCryptoSession9::StartSessionKeyRefresh
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d9.h
api_name:
 - IDirect3DCryptoSession9.StartSessionKeyRefresh
---

# IDirect3DCryptoSession9::StartSessionKeyRefresh


## -description

Gets a random number that can be used to refresh the session key.

## -parameters

### -param pRandomNumber

A pointer to a byte array that receives a random number.

### -param RandomNumberSize

The size of the <i>pRandomNumber</i> array, in bytes. The size should match the size of the session key.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

To generate a new session key, perform a bitwise <b>XOR</b> between the previous session key and the random number. The new session key does not take affect until the application calls <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3dcryptosession9-finishsessionkeyrefresh">IDirect3DCryptoSession9::FinishSessionKeyRefresh</a>.

If the driver supports this method, the driver sets the <b>D3DCPCAPS_FRESHENSESSIONKEY</b> capabilities flag in  the <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-getcontentprotectioncaps">IDirect3DDevice9Video::GetContentProtectionCaps</a> method.

## -see-also

<a href="/windows/desktop/medfound/gpu-based-content-protection">GPU-Based Content Protection</a>



<a href="/windows/desktop/api/d3d9/nn-d3d9-idirect3dcryptosession9">IDirect3DCryptoSession9</a>
