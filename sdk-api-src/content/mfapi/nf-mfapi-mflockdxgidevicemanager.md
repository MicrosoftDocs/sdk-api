---
UID: NF:mfapi.MFLockDXGIDeviceManager
title: MFLockDXGIDeviceManager function (mfapi.h)
description: Locks the shared Microsoft DirectX Graphics Infrastructure (DXGI) Device Manager.
helpviewer_keywords: ["MFLockDXGIDeviceManager","MFLockDXGIDeviceManager function [Media Foundation]","mf.mflockdxgidevicemanager","mfapi/MFLockDXGIDeviceManager"]
old-location: mf\mflockdxgidevicemanager.htm
tech.root: mf
ms.assetid: 01A789BA-C1DE-4EF8-81C4-261F59D5843B
ms.date: 12/05/2018
ms.keywords: MFLockDXGIDeviceManager, MFLockDXGIDeviceManager function [Media Foundation], mf.mflockdxgidevicemanager, mfapi/MFLockDXGIDeviceManager
req.header: mfapi.h
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
req.lib: Mfplat.lib
req.dll: Mfplat.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MFLockDXGIDeviceManager
 - mfapi/MFLockDXGIDeviceManager
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mfplat.dll
api_name:
 - MFLockDXGIDeviceManager
---

# MFLockDXGIDeviceManager function


## -description

Locks the shared Microsoft DirectX Graphics Infrastructure (DXGI) Device Manager.

## -parameters

### -param pResetToken [out]

Receives a token that identifies this instance of the DXGI Device Manager. Use this token when calling <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfdxgidevicemanager-resetdevice">IMFDXGIDeviceManager::ResetDevice</a>.
          This parameter can be <b>NULL</b>.

### -param ppManager [out]

Receives a pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager">IMFDXGIDeviceManager</a> interface. The caller must release the interface.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This function obtains a pointer to a  DXGI Device Manager instance that can be shared between components. The Microsoft Media Foundation platform creates this instance of the  DXGI Device Manager as a singleton object. Alternatively, you can create a new DXGI Device Manager by calling <a href="/windows/desktop/api/mfapi/nf-mfapi-mfcreatedxgidevicemanager">MFCreateDXGIDeviceManager</a>.

The first time this function is called, the Media Foundation platform creates the shared DXGI Device Manager. 

When you are done use the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager">IMFDXGIDeviceManager</a> pointer, call the <a href="/windows/desktop/api/mfapi/nf-mfapi-mfunlockdxgidevicemanager">MFUnlockDXGIDeviceManager</a>.

## -see-also

<a href="/windows/desktop/api/mfapi/nf-mfapi-mfcreatedxgidevicemanager">MFCreateDXGIDeviceManager</a>



<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>