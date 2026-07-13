---
UID: NF:d3d9.IDirect3DCryptoSession9.FinishSessionKeyRefresh
title: IDirect3DCryptoSession9::FinishSessionKeyRefresh (d3d9.h)
description: Switches to a new session key. (IDirect3DCryptoSession9.FinishSessionKeyRefresh)
helpviewer_keywords: ["FinishSessionKeyRefresh","FinishSessionKeyRefresh method [Media Foundation]","FinishSessionKeyRefresh method [Media Foundation]","IDirect3DCryptoSession9 interface","IDirect3DCryptoSession9 interface [Media Foundation]","FinishSessionKeyRefresh method","IDirect3DCryptoSession9.FinishSessionKeyRefresh","IDirect3DCryptoSession9::FinishSessionKeyRefresh","d3d9/IDirect3DCryptoSession9::FinishSessionKeyRefresh","mf.idirect3dcryptosession9_finishsessionkeyrefresh"]
old-location: mf\idirect3dcryptosession9_finishsessionkeyrefresh.htm
tech.root: mf
ms.assetid: b5e4522b-d5a5-4ece-9b78-2cebdf9f9364
ms.date: 12/05/2018
ms.keywords: FinishSessionKeyRefresh, FinishSessionKeyRefresh method [Media Foundation], FinishSessionKeyRefresh method [Media Foundation],IDirect3DCryptoSession9 interface, IDirect3DCryptoSession9 interface [Media Foundation],FinishSessionKeyRefresh method, IDirect3DCryptoSession9.FinishSessionKeyRefresh, IDirect3DCryptoSession9::FinishSessionKeyRefresh, d3d9/IDirect3DCryptoSession9::FinishSessionKeyRefresh, mf.idirect3dcryptosession9_finishsessionkeyrefresh
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
 - IDirect3DCryptoSession9::FinishSessionKeyRefresh
 - d3d9/IDirect3DCryptoSession9::FinishSessionKeyRefresh
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
 - IDirect3DCryptoSession9.FinishSessionKeyRefresh
---

# IDirect3DCryptoSession9::FinishSessionKeyRefresh


## -description

Switches to a new session key.



## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Before calling this method, call the <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3dcryptosession9-startsessionkeyrefresh">IDirect3DCryptoSession9::StartSessionKeyRefresh</a> method. The <b>StartSessionKeyRefresh</b> method gets a random number from the driver, which is used to create a new session key. The new session key does not become active until the application calls  <b>FinishSessionKeyRefresh</b>. After the application calls <b>FinishSessionKeyRefresh</b>, all protected surfaces are encrypted using the new session key.

## -see-also

<a href="/windows/desktop/medfound/gpu-based-content-protection">GPU-Based Content Protection</a>



<a href="/windows/desktop/api/d3d9/nn-d3d9-idirect3dcryptosession9">IDirect3DCryptoSession9</a>
