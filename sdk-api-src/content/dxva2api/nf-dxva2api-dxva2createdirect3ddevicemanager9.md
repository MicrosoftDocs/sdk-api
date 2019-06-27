---
UID: NF:dxva2api.DXVA2CreateDirect3DDeviceManager9
title: DXVA2CreateDirect3DDeviceManager9 function (dxva2api.h)
author: windows-sdk-content
description: Creates an instance of the Direct3D Device Manager.
old-location: mf\dxva2createdirect3ddevicemanager9.htm
tech.root: medfound
ms.assetid: b06e9c68-80ee-4997-bcf7-f05879aa5776
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DXVA2CreateDirect3DDeviceManager9, DXVA2CreateDirect3DDeviceManager9 function [Media Foundation], b06e9c68-80ee-4997-bcf7-f05879aa5776, dxva2api/DXVA2CreateDirect3DDeviceManager9, mf.dxva2createdirect3ddevicemanager9
ms.topic: function
f1_keywords: 
 - "dxva2api/DXVA2CreateDirect3DDeviceManager9"
req.header: dxva2api.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dxva2.lib
req.dll: Dxva2.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - dxva2.dll
api_name:
 - DXVA2CreateDirect3DDeviceManager9
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# DXVA2CreateDirect3DDeviceManager9 function


## -description


Creates an instance of the <a href="https://docs.microsoft.com/windows/desktop/medfound/direct3d-device-manager">Direct3D Device Manager</a>.
        


## -parameters




### -param pResetToken [out]

Receives a token that identifies this instance of the Direct3D device manager. Use this token when calling <a href="https://docs.microsoft.com/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice">IDirect3DDeviceManager9::ResetDevice</a>.
          


### -param ppDeviceManager [out]

Receives a pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9">IDirect3DDeviceManager9</a> interface. The caller must release the interface.
          


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Windows Store apps must use <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager">IMFDXGIDeviceManager</a> and <a href="https://docs.microsoft.com/windows/desktop/medfound/direct3d-11-video-apis">Direct3D 11 Video APIs</a>. 


#### Examples


```cpp
HRESULT CreateD3DDeviceManager(
    IDirect3DDevice9 *pDevice, 
    UINT *pReset, 
    IDirect3DDeviceManager9 **ppManager
    )
{
    UINT resetToken = 0;

    IDirect3DDeviceManager9 *pD3DManager = NULL;

    HRESULT hr = DXVA2CreateDirect3DDeviceManager9(&resetToken, &pD3DManager);

    if (FAILED(hr))
    {
        goto done;
    }

    hr = pD3DManager->ResetDevice(pDevice, resetToken);

    if (FAILED(hr))
    {
        goto done;
    }

    *ppManager = pD3DManager;
    (*ppManager)->AddRef();

    *pReset = resetToken;


done:
    SafeRelease(&pD3DManager);
    return hr;
}

```





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/direct3d-device-manager">Direct3D Device Manager</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>
 

 

