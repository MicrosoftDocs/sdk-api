---
UID: NF:mfapi.MFUnlockDXGIDeviceManager
title: MFUnlockDXGIDeviceManager function (mfapi.h)
description: Unlocks the shared Microsoft DirectX Graphics Infrastructure (DXGI) Device Manager.
helpviewer_keywords: ["MFUnlockDXGIDeviceManager","MFUnlockDXGIDeviceManager function [Media Foundation]","mf.mfunlockdxgidevicemanager","mfapi/MFUnlockDXGIDeviceManager"]
old-location: mf\mfunlockdxgidevicemanager.htm
tech.root: mf
ms.assetid: 89121716-4F30-4ACD-AA48-F563550B94A1
ms.date: 12/05/2018
ms.keywords: MFUnlockDXGIDeviceManager, MFUnlockDXGIDeviceManager function [Media Foundation], mf.mfunlockdxgidevicemanager, mfapi/MFUnlockDXGIDeviceManager
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
 - MFUnlockDXGIDeviceManager
 - mfapi/MFUnlockDXGIDeviceManager
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
 - MFUnlockDXGIDeviceManager
---

# MFUnlockDXGIDeviceManager function


## -description

Unlocks the shared Microsoft DirectX Graphics Infrastructure (DXGI) Device Manager.



## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Call this function after a successful call to the <a href="/windows/desktop/api/mfapi/nf-mfapi-mflockdxgidevicemanager">MFLockDXGIDeviceManager</a> function.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>
