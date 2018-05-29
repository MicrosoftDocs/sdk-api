---
UID: NF:mfapi.MFLockDXGIDeviceManager
title: MFLockDXGIDeviceManager function
author: windows-sdk-content
description: Locks the shared Microsoft DirectX Graphics Infrastructure (DXGI) Device Manager.
old-location: mf\mflockdxgidevicemanager.htm
old-project: medfound
ms.assetid: 01A789BA-C1DE-4EF8-81C4-261F59D5843B
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: MFLockDXGIDeviceManager, MFLockDXGIDeviceManager function [Media Foundation], mf.mflockdxgidevicemanager, mfapi/MFLockDXGIDeviceManager
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
req.typenames: MF_CUSTOM_DECODE_UNIT_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	mfplat.dll
api_name:
-	MFLockDXGIDeviceManager
product: Windows
targetos: Windows
req.lib: Mfplat.lib
req.dll: Mfplat.dll
req.irql: 
req.product: GDI+ 1.1
---

# MFLockDXGIDeviceManager function


## -description


Locks the shared Microsoft DirectX Graphics Infrastructure (DXGI) Device Manager.


## -parameters




### -param pResetToken [out]

Receives a token that identifies this instance of the DXGI Device Manager. Use this token when calling <a href="https://msdn.microsoft.com/D8A2291A-792B-4D24-997A-9C152FFE5426">IMFDXGIDeviceManager::ResetDevice</a>.
          This parameter can be <b>NULL</b>.


### -param ppManager [out]

Receives a pointer to the <a href="https://msdn.microsoft.com/4A0DC266-FCF0-4ECD-AC78-CF429839486D">IMFDXGIDeviceManager</a> interface. The caller must release the interface.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This function obtains a pointer to a  DXGI Device Manager instance that can be shared between components. The Microsoft Media Foundation platform creates this instance of the  DXGI Device Manager as a singleton object. Alternatively, you can create a new DXGI Device Manager by calling <a href="https://msdn.microsoft.com/5398B6D7-1E7D-4987-A163-3360C805EE9C">MFCreateDXGIDeviceManager</a>.

The first time this function is called, the Media Foundation platform creates the shared DXGI Device Manager. 

When you are done use the <a href="https://msdn.microsoft.com/4A0DC266-FCF0-4ECD-AC78-CF429839486D">IMFDXGIDeviceManager</a> pointer, call the <a href="https://msdn.microsoft.com/89121716-4F30-4ACD-AA48-F563550B94A1">MFUnlockDXGIDeviceManager</a>.




## -see-also




<a href="https://msdn.microsoft.com/5398B6D7-1E7D-4987-A163-3360C805EE9C">MFCreateDXGIDeviceManager</a>



<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>
 

 

