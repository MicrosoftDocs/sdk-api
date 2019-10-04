---
UID: NF:mfapi.MFUnlockDXGIDeviceManager
title: MFUnlockDXGIDeviceManager function (mfapi.h)
author: windows-sdk-content
description: Unlocks the shared Microsoft DirectX Graphics Infrastructure (DXGI) Device Manager.
old-location: mf\mfunlockdxgidevicemanager.htm
tech.root: medfound
ms.assetid: 89121716-4F30-4ACD-AA48-F563550B94A1
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: MFUnlockDXGIDeviceManager, MFUnlockDXGIDeviceManager function [Media Foundation], mf.mfunlockdxgidevicemanager, mfapi/MFUnlockDXGIDeviceManager
ms.topic: function
f1_keywords: 
 - "mfapi/MFUnlockDXGIDeviceManager"
dev_langs:
 - c++
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mfplat.dll
api_name:
 - MFUnlockDXGIDeviceManager
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# MFUnlockDXGIDeviceManager function


## -description


Unlocks the shared Microsoft DirectX Graphics Infrastructure (DXGI) Device Manager.


## -parameters






## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Call this function after a successful call to the <a href="https://docs.microsoft.com/windows/desktop/api/mfapi/nf-mfapi-mflockdxgidevicemanager">MFLockDXGIDeviceManager</a> function.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>
 

 

