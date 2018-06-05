---
UID: NF:mfapi.MFUnlockDXGIDeviceManager
title: MFUnlockDXGIDeviceManager function
author: windows-sdk-content
description: Unlocks the shared Microsoft DirectX Graphics Infrastructure (DXGI) Device Manager.
old-location: mf\mfunlockdxgidevicemanager.htm
old-project: medfound
ms.assetid: 89121716-4F30-4ACD-AA48-F563550B94A1
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: MFUnlockDXGIDeviceManager, MFUnlockDXGIDeviceManager function [Media Foundation], mf.mfunlockdxgidevicemanager, mfapi/MFUnlockDXGIDeviceManager
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: mfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: MF_CUSTOM_DECODE_UNIT_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	mfplat.dll
api_name:
-	MFUnlockDXGIDeviceManager
product: Windows
targetos: Windows
req.lib: Mfplat.lib
req.dll: Mfplat.dll
req.irql: 
req.product: GDI+ 1.1
---

# MFUnlockDXGIDeviceManager function


## -description


Unlocks the shared Microsoft DirectX Graphics Infrastructure (DXGI) Device Manager.


## -parameters






## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Call this function after a successful call to the <a href="https://msdn.microsoft.com/01A789BA-C1DE-4EF8-81C4-261F59D5843B">MFLockDXGIDeviceManager</a> function.




## -see-also




<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>
 

 

